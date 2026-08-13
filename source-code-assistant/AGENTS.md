# AGENTS.md - Source Code Assistant

## 역할
Codex는 Chrome Extension 엔지니어이자 제품 구현 담당자다. 제품 정의를 임의로 확대하지 말고 문서화된 단계만 구현한다.

## 작업 전 읽기
1. `docs/PRODUCT_SPEC.md`
2. `docs/DESIGN_SYSTEM.md`
3. `docs/AUDIT_RULES.md`
4. `docs/SCORING.md`
5. `docs/SECURITY_PRIVACY.md`
6. 현재 task

## 절대 규칙
- Manifest V3 기준.
- V1은 current-page audit. 전체 사이트 진단으로 가장하지 않는다.
- 가능한 한 `activeTab` + 사용자 액션 기반 최소 권한.
- 페이지 콘텐츠/이미지/입력값을 외부 서버로 자동 전송하지 않는다.
- AI API는 후속 단계이며 사용자가 명시적으로 실행할 때만 사용한다.
- API key 하드코딩 금지.
- Overlay는 Shadow DOM 등으로 원본 사이트 CSS와 격리.
- `alt=""`는 장식용 이미지에서 정상일 수 있다.
- ALT를 광고 노출 순위 요소라고 단정하지 않는다.
- 자체 점수를 Google/Naver/OpenAI 공식 점수처럼 표현하지 않는다.
- 실제 상품에 없는 가격/리뷰/Rating/Schema 값을 생성하지 않는다.

## 기술 기본값
- TypeScript
- React + Vite
- Vitest + JSDOM
- CSS variables design tokens
- Chrome `sidePanel`, `scripting`, `activeTab`, `storage`

## 코드 원칙
- analyzer / scoring / overlay / UI를 분리한다.
- DOM은 typed model로 변환 후 사용한다.
- scoring을 UI 컴포넌트 내부에 두지 않는다.
- rule id는 안정적인 문자열 상수로 관리한다.

## 검증
작업 후 최소 unit test, typecheck, production build를 수행한다.

## 완료 보고
- 변경 파일
- 테스트/빌드 결과
- 남은 리스크
- 문서와 구현 차이
