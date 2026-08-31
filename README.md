# 주식사주 개인정보처리방침

**최종 수정일: 2026년 8월 31일**

무당 스튜디오(이하 "개발자")가 만든 안드로이드 앱 **주식사주**(패키지 이름
`com.mudangstudio.stocksaju`, 이하 "앱")의 개인정보 처리 방침입니다.

웹에서 보기: <https://ted19.github.io/stocksaju-privacy/>

---

## 한 줄 요약

**주식사주는 개인정보를 수집하지 않습니다.** 회원가입도, 개발자가 운영하는
서버도, 광고도, 분석 도구도 없습니다. 앱이 인터넷에 접속하는 것은
금융감독원·금융위원회·한국거래소가 공개한 공시와 시세를 내려받을 때뿐이며,
그때도 사용자를 식별하는 정보는 보내지 않습니다.

---

## 1. 수집하는 개인정보

**없습니다.**

앱은 회원가입이 없고, 계정을 만들지 않으며, 이름·이메일·전화번호·생년월일·
광고 식별자·위치 정보 등 어떤 정보도 수집하지 않습니다. 개발자가 운영하는
서버가 존재하지 않으므로 사용자의 정보를 전송받을 곳 자체가 없습니다.

## 2. 기기에 저장되는 정보

앱은 아래 정보를 **사용자 기기 내부 저장소에만** 보관합니다. 이 정보는 기기를
떠나지 않으며 개발자에게 전송되지 않습니다.

| 저장 항목 | 내용 |
|---|---|
| 관심종목 | 사용자가 추가한 종목 코드와 추가한 시각 |
| 공시·재무 자료 | 조회한 기업의 공개 재무제표, 지분공시, 일별 시세 |
| 종목 목록 | 공시 대상 법인의 이름과 종목 코드 (공개 자료) |
| 지난 기록 | 뽑은 타로 카드, 주역 동전 결과, 분석 결과 (최대 200건, 넘으면 오래된 것부터 지워집니다) |
| 프로필 | 사용자가 직접 입력한 별칭(선택 사항)과 투자 성향(공격적·중립·보수적) |
| 보유 정보 | 사용자가 직접 입력한 평단가와 수량 (선택 사항) |
| 오픈API 인증키 | 사용자가 각 기관에서 직접 발급받아 입력한 인증키 |

인증키는 다른 자료와 달리 **안드로이드 키스토어로 암호화되는 보안 저장소**에
따로 보관하며, 한 번 입력한 뒤에는 화면에 다시 꺼내 보여주지 않습니다. 앱
설치 파일이나 로그에도 남기지 않습니다.

## 3. 앱이 접속하는 곳

앱은 아래 세 곳의 공개 API에만 접속합니다.

| 주소 | 제공 기관 | 용도 |
|---|---|---|
| `opendart.fss.or.kr` | 금융감독원 DART 오픈API | 공시 재무제표, 지분공시 |
| `apis.data.go.kr` | 공공데이터포털 (금융위원회 주식시세정보) | 일별 시세 |
| `data-dbg.krx.co.kr` | 한국거래소 | 일별 시세 (금융위 대신 쓸 수 있는 경로) |

요청에 담기는 것은 **사용자가 입력한 인증키와 조회할 종목·법인 코드뿐**입니다.
별칭, 투자 성향, 지난 기록, 관심종목 목록은 어디로도 나가지 않습니다.

각 기관은 요청을 처리하면서 자체 정책에 따라 인증키별 이용 내역을 남길 수
있습니다. 이는 사용자가 해당 기관에서 직접 발급받은 인증키에 대한 일이며, 각
기관의 이용약관과 개인정보 처리방침을 따릅니다.

## 4. 제3자 제공 및 위탁

**없습니다.** 앱은 어떤 정보도 제3자에게 제공하거나 처리를 위탁하지 않습니다.

## 5. 광고 및 분석 도구

앱에는 **광고가 없으며, 분석·추적 도구를 사용하지 않습니다.** Google
Analytics, Firebase, 광고 SDK, 크래시 리포트 도구 등 사용자 행동을 수집하는
어떤 외부 도구도 포함되어 있지 않습니다.

## 6. 앱이 요청하는 권한

`INTERNET` 한 가지뿐이며, 위 3항의 공개 API에 접속하는 데에만 씁니다. 카메라,
연락처, 위치, 저장소, 마이크 등 다른 어떤 권한도 요청하지 않습니다.

## 7. 정보의 삭제

사용자는 언제든 저장된 정보를 앱 안에서 직접 지울 수 있습니다.

- **관심종목** — 목록의 카드마다 있는 휴지통 단추
- **기록 하나씩** — 기록 화면에서 항목마다 "이 기록 지우기"
- **기록 종류별·전체** — 기록 화면의 "기록 전체 지우기"
- **인증키** — 인증키 화면에서 항목마다 "삭제"
- **별칭** — 프로필 화면에서 입력란을 비우고 저장
- **전부** — 앱을 삭제하면 위 모든 정보가 기기에서 함께 제거됩니다

앱이 정보를 외부에 보관하지 않으므로, 개발자에게 삭제를 요청할 대상 자체가
없습니다.

## 8. 아동의 개인정보

앱은 만 14세 미만 아동을 대상으로 하지 않습니다. 앱이 어떤 정보도 수집하지
않으므로 아동으로부터 수집되는 정보 또한 없습니다.

## 9. 투자에 관한 고지

앱이 보여주는 점수와 해설은 공개된 공시·시세 자료를 가공한 참고 자료이며,
타로와 주역은 재미로 보는 것입니다. **어느 쪽도 투자 자문이 아니며 투자 판단의
근거로 쓰기 위한 것이 아닙니다.** 투자의 책임은 사용자 본인에게 있습니다.

## 10. 방침의 변경

이 방침이 바뀌면 이 문서를 갱신하고 최종 수정일을 바꿉니다. 수집 항목이 새로
생기는 등 중요한 변경이 있을 경우 앱 업데이트 내용에도 함께 알립니다.

## 11. 문의

개인정보 처리에 관한 문의는 아래로 연락해 주세요.

- 개발자: 무당 스튜디오
- 이메일: adinfototo@gmail.com

---

# Privacy Policy (English)

**Last updated: August 31, 2026**

This is the privacy policy for **Stock Saju** (Korean title 주식사주, package
`com.mudangstudio.stocksaju`), an Android app by Mudang Studio.

**Stock Saju does not collect any personal information.** There are no accounts,
no developer-operated servers, no ads, and no analytics. The app connects to the
internet only to download public disclosure and market data published by Korean
financial authorities, and those requests carry nothing that identifies you.

The app stores the following **only in your device's local storage**: your
watchlist, the public financial data it downloaded for companies you looked up,
your reading history (tarot cards, I Ching coin tosses, and analysis results — up
to 200 entries), an optional nickname, an investment stance, an optional average
purchase price and share count you type in yourself, and the Open API keys
you obtained yourself and entered. API keys are held in secure storage encrypted
by the Android Keystore and are never shown again once entered.

The app connects only to `opendart.fss.or.kr` (Financial Supervisory Service),
`apis.data.go.kr` (Financial Services Commission stock price data), and
`data-dbg.krx.co.kr` (Korea Exchange). Requests carry only the API key you entered
and the stock or corporation code being looked up. Nothing is shared with third
parties, and no analytics or advertising SDK is included.

You can delete everything from inside the app — the watchlist trash button,
per-entry and bulk history deletion, API key deletion, and clearing the nickname.
Uninstalling the app removes all of it. Because nothing is kept outside your
device, there is no data held by the developer for you to request deletion of.

The only permission requested is `INTERNET`, used solely for the APIs above. The
app is not directed at children under 14.

The scores and commentary the app shows are reference material derived from public
data, and the tarot and I Ching features are for entertainment. Neither is
investment advice.

If this policy changes, this document will be updated and the date above revised.

Contact: Mudang Studio — adinfototo@gmail.com
