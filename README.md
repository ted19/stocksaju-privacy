# 주식 사주 개인정보처리방침

> **이 브랜치(`ads-revision`)는 아직 배포본이 아닙니다.**
> 광고를 켠 버전을 스토어에 올리는 시점에 `main` 으로 병합하세요.
> 자세한 절차는 [REVISION-NOTES.md](REVISION-NOTES.md) 를 보세요.

**최종 수정일: 0000년 0월 0일 (광고 포함 버전 배포일로 교체)**

무당 스튜디오(이하 "개발자")가 만든 안드로이드 앱 **주식 사주**(패키지 이름
`com.dalcomsoft.stock`, 이하 "앱")의 개인정보 처리 방침입니다.

웹에서 보기: <https://ted19.github.io/stocksaju-privacy/>

---

## 한 줄 요약

**개발자는 어떤 정보도 수집하지 않습니다. 다만 화면 아래 배너 광고를 위해
Google 이 광고 식별자를 비롯한 정보를 수집합니다.** 회원가입도, 개발자가
운영하는 서버도, 분석·추적 도구도 없습니다. 관심종목·기록·프로필·인증키는 전부
기기 안에만 남습니다.

---

## 1. 개발자가 수집하는 개인정보

**없습니다.** 앱은 회원가입이 없고, 계정을 만들지 않으며, 이름·이메일·전화번호·
생년월일·위치 정보 등을 수집하지 않습니다. 개발자가 운영하는 서버가 존재하지
않으므로 사용자의 정보를 전송받을 곳 자체가 없습니다.

**광고는 예외입니다.** 앱에 실린 Google AdMob 이 광고를 띄우기 위해 정보를
수집하며, 그 내용은 4항에 있습니다. 개발자는 그 값을 직접 받아 보지 않고
Google 이 주는 집계된 수익 통계만 봅니다.

## 2. 기기에 저장되는 정보

앱은 아래 정보를 **사용자 기기 내부 저장소에만** 보관합니다. 이 정보는 기기를
떠나지 않으며 개발자에게도, 광고 회사에도 전송되지 않습니다.

| 저장 항목 | 내용 |
|---|---|
| 관심종목 | 사용자가 추가한 종목 코드와 추가한 시각 |
| 공시·재무 자료 | 조회한 기업의 공개 재무제표, 지분공시, 일별 시세 |
| 종목 목록 | 공시 대상 법인의 이름과 종목 코드 (공개 자료) |
| 지난 기록 | 뽑은 타로 카드, 주역 동전 결과, 분석 결과 (최대 200건, 넘으면 오래된 것부터 지워집니다) |
| 프로필 | 사용자가 직접 입력한 별칭(선택 사항)과 투자 성향(공격적·중립·보수적) |
| 오픈API 인증키 | 사용자가 각 기관에서 직접 발급받아 입력한 인증키 |

인증키는 다른 자료와 달리 **안드로이드 키스토어로 암호화되는 보안 저장소**에
따로 보관하며, 한 번 입력한 뒤에는 화면에 다시 꺼내 보여주지 않습니다. 앱
설치 파일이나 로그에도 남기지 않습니다.

## 3. 앱이 접속하는 곳

| 주소 | 제공 기관 | 용도 |
|---|---|---|
| `opendart.fss.or.kr` | 금융감독원 DART 오픈API | 공시 재무제표, 지분공시 |
| `apis.data.go.kr` | 공공데이터포털 (금융위원회 주식시세정보) | 일별 시세 |
| `data-dbg.krx.co.kr` | 한국거래소 | 일별 시세 (금융위 대신 쓸 수 있는 경로) |
| Google 광고 서버 | Google (AdMob) | 배너 광고 요청과 표시 |

공공 API 요청에 담기는 것은 **사용자가 입력한 인증키와 조회할 종목·법인
코드뿐**입니다. 별칭, 투자 성향, 지난 기록, 관심종목 목록은 어디로도 나가지
않습니다.

각 기관은 요청을 처리하면서 자체 정책에 따라 인증키별 이용 내역을 남길 수
있습니다. 이는 사용자가 해당 기관에서 직접 발급받은 인증키에 대한 일이며, 각
기관의 이용약관과 개인정보 처리방침을 따릅니다.

## 4. 광고

앱 화면 맨 아래에 **Google AdMob 배너 광고 하나**가 붙습니다. 광고를 띄우는
과정에서 Google 은 아래 정보를 수집·이용합니다.

- **광고 식별자(AAID)** — 기기마다 하나씩 있는, 사용자가 언제든 초기화할 수 있는 번호
- **기기·운영체제 정보** — 모델, 안드로이드 버전, 화면 크기, 언어 설정 등
- **IP 주소에서 유추한 대략적인 위치** — 도시 수준이며, 앱은 위치 권한을 요청하지 않습니다
- **광고 상호작용** — 광고가 보였는지, 눌렸는지

이 정보는 Google 로 바로 전송되며 개발자를 거치지 않습니다. Google 의 처리
방식은 [Google 이 파트너 사이트·앱에서 정보를 사용하는 방법](https://policies.google.com/technologies/partner-sites)과
[Google 개인정보처리방침](https://policies.google.com/privacy)을 보세요.

**광고 개인 맞춤을 끄거나 식별자를 지울 수 있습니다.** 안드로이드
*설정 → 보안 및 개인정보 보호 → 개인정보 보호 → 광고* 에서 광고 ID 를
초기화하거나 삭제하면 됩니다. 삭제해도 광고는 계속 보이지만 맞춤형이 아닌
광고가 나옵니다.

앱은 **관심종목, 지난 기록, 프로필, 인증키를 광고에 쓰지 않으며** 광고 회사에
넘기지도 않습니다.

## 5. 제3자 제공 및 위탁

광고를 위해 4항의 정보가 **Google** 에 전달됩니다. 그 밖에는 어떤 정보도
제3자에게 제공하거나 처리를 위탁하지 않습니다.

## 6. 분석 도구

앱은 **분석·추적 도구를 사용하지 않습니다.** Google Analytics, Firebase
Analytics, 크래시 리포트 도구 등 사용자 행동을 수집하는 도구는 포함되어 있지
않습니다. 외부로 나가는 것은 4항의 광고 관련 정보뿐입니다.

## 7. 앱이 요청하는 권한

사용자에게 따로 묻는 권한은 없습니다. 설치 시 아래 항목이 선언됩니다.

| 권한 | 쓰임 |
|---|---|
| `INTERNET` | 공시·시세 조회, 광고 요청 |
| `ACCESS_NETWORK_STATE` | 광고 SDK 가 연결 상태를 확인 |
| `com.google.android.gms.permission.AD_ID` | 광고 식별자 읽기 |
| `ACCESS_ADSERVICES_AD_ID`<br>`ACCESS_ADSERVICES_ATTRIBUTION`<br>`ACCESS_ADSERVICES_TOPICS` | 안드로이드 개인정보 보호 샌드박스의 광고 기능 |
| `WAKE_LOCK`<br>`FOREGROUND_SERVICE` | 광고 SDK 가 함께 선언하는 항목 |

`INTERNET` 을 뺀 나머지는 모두 Google Mobile Ads SDK 가 더하는 것입니다.
카메라, 연락처, 위치, 저장소, 마이크 등 다른 어떤 권한도 요청하지 않습니다.

## 8. 정보의 삭제

사용자는 언제든 저장된 정보를 앱 안에서 직접 지울 수 있습니다.

- **관심종목** — 목록의 카드마다 있는 휴지통 단추
- **기록 하나씩** — 기록 화면에서 항목마다 "이 기록 지우기"
- **기록 종류별·전체** — 기록 화면의 "기록 전체 지우기"
- **인증키** — 인증키 화면에서 항목마다 "삭제"
- **별칭** — 프로필 화면에서 입력란을 비우고 저장
- **광고 식별자** — 안드로이드 설정에서 초기화·삭제 (4항)
- **전부** — 앱을 삭제하면 기기에 저장된 위 정보가 모두 제거됩니다

개발자가 보관하는 정보가 없으므로 개발자에게 삭제를 요청할 대상이 없습니다.
Google 이 광고 목적으로 보관한 정보에 대한 요청은 Google 의 개인정보처리방침에
안내된 절차를 따릅니다.

## 9. 아동의 개인정보

앱은 만 14세 미만 아동을 대상으로 하지 않으며, 아동을 대상으로 한 광고를
요청하지 않습니다. 개발자가 아동으로부터 수집하는 정보는 없습니다.

## 10. 투자에 관한 고지

앱이 보여주는 점수와 해설은 공개된 공시·시세 자료를 가공한 참고 자료이며,
타로와 주역은 재미로 보는 것입니다. **어느 쪽도 투자 자문이 아니며 투자 판단의
근거로 쓰기 위한 것이 아닙니다.** 투자의 책임은 사용자 본인에게 있습니다.
앱에 실린 광고는 개발자가 고른 것이 아니며 광고 내용에 대한 보증도 아닙니다.

## 11. 방침의 변경

이 방침이 바뀌면 이 문서를 갱신하고 최종 수정일을 바꿉니다. 수집 항목이 새로
생기는 등 중요한 변경이 있을 경우 앱 업데이트 내용에도 함께 알립니다.

## 12. 문의

개인정보 처리에 관한 문의는 아래로 연락해 주세요.

- 개발자: 무당 스튜디오
- 이메일: adinfototo@gmail.com

---

# Privacy Policy (English)

**Last updated: (replace with the release date of the ad-enabled version)**

This is the privacy policy for **Stock Saju** (Korean title 주식 사주, package
`com.dalcomsoft.stock`), an Android app by Mudang Studio.

**The developer collects nothing. Google, however, collects an advertising
identifier and related data to serve the banner ad at the bottom of the screen.**
There are no accounts, no developer-operated servers, and no analytics.

The app stores your watchlist, downloaded public financial data, reading history
(up to 200 entries), an optional nickname, an investment stance, and the Open API
keys you entered — **all only on your device**. API keys are held in secure
storage encrypted by the Android Keystore.

The app connects to `opendart.fss.or.kr`, `apis.data.go.kr`, and
`data-dbg.krx.co.kr` for public disclosure and price data, and to Google's ad
servers for advertising. Public-API requests carry only your API key and the code
being looked up.

For advertising, Google collects your advertising identifier (AAID), device and
OS information, approximate location inferred from your IP address, and ad
interactions. This goes directly to Google; the developer sees only aggregate
revenue figures. See [How Google uses information from sites or apps that use our
services](https://policies.google.com/technologies/partner-sites) and the
[Google Privacy Policy](https://policies.google.com/privacy). You can reset or
delete the advertising identifier under Android *Settings → Security & privacy →
Privacy → Ads*.

Beyond the advertising data above, nothing is shared with third parties. The app
uses no analytics or tracking tools.

Permissions declared: `INTERNET`, `ACCESS_NETWORK_STATE`,
`com.google.android.gms.permission.AD_ID`, `ACCESS_ADSERVICES_AD_ID`,
`ACCESS_ADSERVICES_ATTRIBUTION`, `ACCESS_ADSERVICES_TOPICS`, `WAKE_LOCK`, and
`FOREGROUND_SERVICE`. Everything except `INTERNET` is added by the Google Mobile
Ads SDK. No camera, contacts, location, storage, or microphone permission is
requested.

You can delete everything from inside the app; uninstalling removes all of it.
The app is not directed at children under 14.

The scores and commentary are reference material derived from public data, and
the tarot and I Ching features are for entertainment. Neither is investment
advice. Ads are not chosen by the developer and are not endorsements.

Contact: Mudang Studio — adinfototo@gmail.com
