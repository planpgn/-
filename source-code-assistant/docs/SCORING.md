# Scoring

## 점수명
- V1: **Page AI Readiness**
- V2 Deep Scan: **Site AI Readiness**

혼용 금지.

## 중요 고지
Source Code Assistant 자체 진단 지표다.
- Google 공식 SEO 점수 아님
- Naver 광고 품질/순위 점수 아님
- OpenAI 광고 선출 점수 아님
- ALT/Schema 개선만으로 CTR/CVR/ROAS 상승을 보장하지 않음

## V1 가중치
| 영역 | 가중치 |
|---|---:|
| Semantic Image Layer | 30 |
| Structured Data | 25 |
| Metadata | 20 |
| Content Structure | 15 |
| Consistency | 10 |

Crawlability는 current-page local scan으로 충분히 검증할 수 없으므로 V1 총점에 억지로 넣지 않는다.

## 계산 원칙
- applicable rules만 분모에 사용
- N/A는 0점 처리하지 않음
- Critical > Warning > Info
- 동일 element에 중복 penalty 과다 적용 금지
- 초기 권장: Critical 100% 손실, Warning 50%, Info 영향 없음

## 결과 UI
`68 / 100 · 현재 DOM 기준`
`Critical 4 · Warning 11 · Passed 27`

총점보다 개선 우선순위 3개를 함께 보여준다.
