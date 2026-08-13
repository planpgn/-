# 3-Round Review

## Round 1 - 기술 주장 검토
문제: ALT가 없으면 AI가 이미지를 못 읽는다고 단정하면 과장. 장식용 `alt=""` false positive, AI API/보안/비용을 V1부터 넣는 문제, 현재 페이지와 전체 사이트 진단 혼재.

반영: ALT를 semantic signal 중 하나로 정의. decorative empty ALT 예외. V1 AI API 제거. Page/Site Readiness 분리. 자체 점수 비공식 고지.

## Round 2 - 영업 UX 검토
문제: broad 권한, overlay CSS 충돌, score 과대강조, 동적 페이지 재진단 부재, 기술정보와 영업정보 혼재.

반영: activeTab 최소 권한, Shadow DOM overlay, score보다 Critical/Warning/우선순위 강조, `다시 진단`, Sales View + Developer expander 분리.

## Round 3 - Codex 개발 운영 검토
문제: 초기 기능 팽창, site crawl/AI suggestion 동시 구현 시 테스트 난이도 상승, UI만 먼저 완성될 위험.

최종: Phase 1은 `현재 페이지 Scan + Image audit + Side Panel`; Phase 2 Schema/Metadata; Phase 3 Overlay; 이후 AI Vision/SearchTune API. analyzer/scoring/overlay/UI 모듈 분리 및 fixture 테스트를 필수화한다.
