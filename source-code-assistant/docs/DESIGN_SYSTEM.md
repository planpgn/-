# Design System

## 방향
SearchTune OS 제안서의 시각 언어를 기반으로 하되 그대로 복제하지 않는다.

반영 요소:
- 짙은 네이비 기반
- 선명한 블루 accent
- 큰 헤드라인 + 작은 설명 위계
- 카드 기반 정보 구조
- score ring / status 숫자 중심 표현
- 넓은 여백과 얇은 border

Source Code Assistant는 여기에 selector, raw HTML snippet, rule id 등 technical layer를 추가한다. 영업 기본 화면에서는 `문제 -> 의미 -> 조치`를 우선한다.

## Tokens
```css
:root {
  --sca-navy-950: #070B24;
  --sca-navy-900: #0D1438;
  --sca-navy-800: #151F5A;
  --sca-blue-500: #3858F0;
  --sca-blue-400: #6880F5;
  --sca-bg-light: #F6F7FB;
  --sca-surface-light: #FFFFFF;
  --sca-text-dark: #0B102B;
  --sca-text-light: #F7F8FF;
  --sca-text-muted-dark: #98A4C8;
  --sca-border-dark: rgba(150,165,220,.22);
  --sca-border-light: #E7EAF3;
  --sca-pass: #46C7F4;
  --sca-warning: #FFC94A;
  --sca-critical: #FF6B6B;
  --sca-radius-sm: 8px;
  --sca-radius-md: 14px;
  --sca-radius-lg: 20px;
}
```

## Typography
`Pretendard, "Noto Sans KR", Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`

- Display 28-34 / 700-800
- Section 18-22 / 700
- Card 14-16 / 650-700
- Body 13-14 / 400-500
- Meta/code 11-12 / monospace

## Side Panel
권장 420px, 320-600px responsive.

- Header 56px
- Page identity card
- Score hero
- Critical/Warning/Passed 3 columns
- Sticky tabs
- Scrollable audit list
- Bottom action bar

## Audit Row
1. severity dot
2. issue title
3. 현재 값
4. 이유
5. 권장 조치
6. `페이지에서 보기`
7. Developer expander: selector / HTML snippet

## Overlay
- 2px outline
- 작은 badge
- hover tooltip
- 최대 동시 badge 수 제한
- off 즉시 복구
- Shadow DOM isolation

## 금지
- neon/glass 효과 과다
- 모든 정보를 한 화면에 노출
- 빨간색 정상 상태 사용
- 10px 이하 본문
- SearchTune 로고를 제품 로고처럼 오용
