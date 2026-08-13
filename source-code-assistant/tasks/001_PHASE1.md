# Task 001 - Phase 1

## 목적
Chrome에서 바로 시연 가능한 최소 신뢰 버전을 만든다.

## 구현 순서
1. TypeScript + React + Vite extension scaffold
2. Manifest V3 + Side Panel
3. `activeTab` 기반 current-page scan
4. Image collector를 typed model로 변환
5. `AUDIT_RULES.md`의 Image ALT 규칙 구현
6. Overview + Images UI
7. row -> page element focus/highlight
8. fixture/unit tests

## 테스트 케이스
- alt attribute 없음
- `alt=""`
- filename ALT
- generic ALT
- duplicate ALT
- semantic ALT
- decorative/presentation 이미지
- broken image 가능한 범위

## Acceptance
- unpacked extension으로 로드 가능
- 일반 HTTPS 페이지에서 side panel scan 성공
- 외부 네트워크 요청 없음
- broad host permission 없음
- 결과 deterministic
- decorative empty alt를 Critical로 잡지 않음
- typecheck/test/build 성공

## 이후
Phase 1 완료 후에만 Schema/Metadata, Overlay, Deep Scan/AI 순으로 확장한다.
