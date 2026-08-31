# 광고 반영 개정문 — 배포 절차

이 브랜치(`ads-revision`)는 **광고를 켠 버전을 스토어에 올릴 때** 쓸 방침입니다.
지금 `main` 이 서비스 중인 방침은 광고가 없는 현재 배포본에 맞는 내용이므로
그대로 두세요.

`main` 을 먼저 병합하면 **아직 광고가 없는 앱에 대해 광고가 있다고 적는 셈**이
되어 그것대로 부정확합니다. 순서를 지켜야 합니다.

## 순서

1. 앱에서 광고를 켜고 빌드한다.

   ```
   flutter build appbundle \
     --dart-define=ADS_ENABLED=true \
     --dart-define=ADMOB_BANNER_ID=ca-app-pub-XXXXXXXX/YYYYYYYY
   ```

   빌드 전에 `android/app/src/main/AndroidManifest.xml` 의
   `com.google.android.gms.ads.APPLICATION_ID` 를 실제 AdMob 앱 ID 로 바꿀 것.
   이 값은 네이티브가 읽으므로 dart-define 이 닿지 않는다.

2. 이 브랜치의 날짜 자리를 실제 배포일로 바꾼다. 세 군데다.

   - `privacy.html` — 한국어 `<p class="date">`
   - `privacy.html` — 영어 `<p class="date">`
   - `README.md` — 상단 "최종 수정일"과 영문 "Last updated"

   `0000년 0월 0일` 과 `(replace with ...)` 로 찾으면 된다.

3. `README.md` 맨 위의 "이 브랜치는 아직 배포본이 아닙니다" 안내 블록을 지운다.

4. `main` 에 병합하고 푸시한다. GitHub Pages 가 자동으로 다시 빌드한다.

   ```
   git checkout main
   git merge ads-revision
   git push
   ```

5. 스토어 심사에 앱을 제출한다. 방침이 먼저 올라가 있어야 한다.

## 함께 고쳐야 하는 것 — Play 콘솔 데이터 보안

방침만 고치면 끝이 아닙니다. Play 콘솔의 **데이터 보안(Data safety)** 신고를
광고에 맞춰 갱신해야 합니다. 신고 내용과 방침이 어긋나면 심사에서 반려됩니다.

- 수집 항목에 **기기 또는 기타 ID**(광고 ID) 추가
- 목적: **광고 또는 마케팅**
- 제3자와 공유: **예** (Google)
- 앱에 광고가 포함되는지: **예**

## 확인해 두지 않은 것 — 유럽 사용자 동의

앱을 **유럽 경제 지역(EEA)·영국**에 배포한다면 광고 노출 전에 사용자 동의를
받아야 하며(GDPR), Google 은 이를 위해 UMP(User Messaging Platform) SDK 를
요구합니다. **현재 앱에는 동의 화면이 구현되어 있지 않습니다.**

- 한국에만 배포한다면 지금 상태로 문제 없습니다.
- EEA·영국에 배포한다면 UMP 연동이 먼저 필요하고, 그때 이 방침에도
  동의 철회 방법을 적는 항목을 추가해야 합니다.

## main 과 달라지는 부분 요약

| 항목 | main (현재 배포본) | ads-revision |
|---|---|---|
| 한 줄 요약 | 정보를 수집하지 않음 | 개발자는 수집 안 함 + Google 이 광고용으로 수집 |
| 광고 | "광고가 없으며" | 4항 신설 — AdMob 배너 하나, 수집 항목과 광고 ID 삭제 방법 |
| 제3자 제공 | 없음 | Google 에 광고 정보 전달 |
| 권한 | `INTERNET` 하나 | 실측 8개 (`INTERNET` 외 7개는 광고 SDK 가 추가) |
| 항목 수 | 11개 | 12개 |

권한 목록은 추측이 아니라 광고를 넣고 빌드한 APK 를
`aapt2 dump badging` 으로 읽어 확인한 값입니다.
