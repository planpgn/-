# Source Code Assistant

> 사람에게 보이는 웹페이지와 AI/검색 시스템이 읽을 수 있는 machine-readable layer의 차이를 시각적으로 보여주는 Chrome 확장프로그램.

## 제품 목적

Source Code Assistant는 영업/마케팅/웹 운영자가 개발자도구를 직접 열지 않고도 현재 보고 있는 웹페이지의 HTML 의미 구조를 빠르게 점검하도록 돕는 진단 도구다.

핵심 경험은 두 가지다.

1. **Side Panel 진단**: 현재 페이지의 이미지 ALT, 메타데이터, 제목 구조, JSON-LD/Schema, 주요 콘텐츠 정합성을 요약한다.
2. **AI View Overlay**: 실제 페이지 위에 문제 이미지/요소를 하이라이트하여 고객에게 현장에서 문제를 바로 설명할 수 있게 한다.

## 핵심 포지셔닝

- 단순 ALT Checker가 아니다.
- 공식 Google/Naver/OpenAI 점수나 광고 랭킹을 재현한다고 주장하지 않는다.
- "Website AI Readiness"를 설명 가능한 자체 규칙으로 진단하는 **영업 + 기술 점검 도구**다.
- V1은 **현재 페이지 로컬 진단**에 집중하고, 사이트 전체 크롤링과 AI Vision은 후속 단계로 분리한다.

## 기본 제품명

- Product: **Source Code Assistant**
- Korean display: **소스코드 어시스턴트**
- Tagline: **AI가 읽는 웹사이트 레이어를 눈에 보이게.**

## 저장소 사용법

Codex로 작업하기 전 반드시 `AGENTS.md`와 `docs/INDEX.md`를 읽는다.
첫 구현은 `prompts/CODEX_BOOTSTRAP.md`를 그대로 시작 프롬프트로 사용한다.

## 문서 지도

- `AGENTS.md` - Codex 상시 운영 규칙
- `docs/PRODUCT_SPEC.md` - 제품 범위와 UX
- `docs/DESIGN_SYSTEM.md` - SearchTune 계열 시각 언어를 반영한 디자인 시스템
- `docs/ARCHITECTURE.md` - Chrome MV3 구조와 데이터 흐름
- `docs/AUDIT_RULES.md` - 진단 규칙
- `docs/SCORING.md` - 점수 체계와 금지 주장
- `docs/SECURITY_PRIVACY.md` - 권한, 데이터 처리, API 보안
- `docs/SALES_DEMO.md` - 영업 현장 사용 흐름
- `docs/REVIEW_3_ROUNDS.md` - 3회 비판/보완 결과
- `docs/SOURCE_NOTES.md` - 기획자료에서 가져온 근거 범위
- `tasks/` - Codex 단계별 구현 태스크
