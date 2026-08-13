# Codex Bootstrap Prompt

Source Code Assistant Phase 1을 구현해줘.

먼저 반드시 읽어:
1. `AGENTS.md`
2. `docs/PRODUCT_SPEC.md`
3. `docs/DESIGN_SYSTEM.md`
4. `docs/AUDIT_RULES.md`
5. `docs/SCORING.md`
6. `docs/SECURITY_PRIVACY.md`
7. `tasks/001_PHASE1.md`

이번 범위는 Phase 1만이다.

필수 결과:
- Manifest V3 Chrome extension
- toolbar icon 클릭 -> Side Panel open
- Side Panel에서 현재 탭 `진단 시작`
- activeTab DOM에서 `<img>` 수집
- ALT missing / empty-review / filename-like / generic / duplicate / broken 규칙
- Overview: total images, issue counts, Image Readiness
- Images 탭: 문제/현재 ALT/src
- `페이지에서 보기`: 해당 이미지 scroll + temporary highlight
- local-only, 외부 API 호출 금지
- broad host permissions 금지
- TypeScript + React + Vite + Vitest
- fixture tests

디자인은 SearchTune에서 파생한 `docs/DESIGN_SYSTEM.md`를 따른다. 장식/애니메이션보다 analyzer 정확도를 우선한다.

완료 전 typecheck, unit test, production build를 실행하고 변경 파일/테스트/남은 리스크를 보고해.
