# Product Spec

## 제품명
**Source Code Assistant / 소스코드 어시스턴트**

Tagline: **AI가 읽는 웹사이트 레이어를 눈에 보이게.**

## 문제 정의
자사몰/랜딩페이지는 사람 눈에는 충분한 정보가 있어 보여도 HTML의 machine-readable layer는 비어 있거나 품질이 낮을 수 있다. 개발자도구에 익숙하지 않은 AE/마케터는 이를 현장에서 설명하기 어렵다.

Source Code Assistant는 현재 보고 있는 페이지를 영업 현장에서 즉시 진단하고, 문제 요소를 실제 화면 위에 표시하는 Chrome 확장프로그램이다.

## V1 핵심 경험
1. 고객 페이지를 연다.
2. 확장프로그램 아이콘을 클릭한다.
3. Side Panel에서 `현재 페이지 진단` 실행.
4. 현재 DOM에서 이미지, 메타, 제목, JSON-LD 등을 수집.
5. Overview / Images / Schema / Metadata / Content 탭으로 결과 표시.
6. `AI View`를 켜면 실제 페이지 위 문제 element에 badge/outline 표시.
7. 결과 복사/JSON 내보내기.

## V1 범위
- current-page local audit
- Image ALT 품질 점검
- Metadata 점검
- JSON-LD / Product schema 점검
- 간단한 visible data ↔ schema consistency
- Page AI Readiness 점수
- Side Panel + Overlay

## V1 비범위
- 전체 사이트 자동 크롤링
- AI Vision ALT 자동 생성
- DOM 자동 수정/배포
- 회원/결제
- 공식 검색/광고 점수 재현

## V2
- SearchTune API 또는 별도 backend 기반 Deep Scan
- robots/crawler 접근성
- AI Vision + Page Context + Brand Context ALT suggestion
- CSV export
- Re-scan 비교

## V3
- 조직/계정
- Audit history
- 고객 리포트 공유
- 개발 적용용 snippet

## 성공 지표
- 1페이지 진단 완료 시간
- false positive 비율
- 문제 element 탐지 정확도
- 영업 데모에서 설명까지 걸리는 시간
- 개발팀에 전달 가능한 actionable issue 비율
