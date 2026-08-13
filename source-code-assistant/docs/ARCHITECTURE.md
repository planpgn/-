# Architecture

Manifest V3 Chrome Extension.

```text
Toolbar Action
 -> Service Worker
    -> Side Panel
    -> activeTab + scripting
       -> Collector / Analyzer
          -> typed AuditResult
             -> Side Panel UI
             -> Overlay Controller
```

## 기본 구성
- Side Panel: 진단 결과 메인 UI
- Service Worker: action/side panel/message routing
- Injected analyzer: images, title/meta/canonical/OG, headings, JSON-LD, visible context 수집
- Overlay Controller: 문제 element annotation. analyzer와 분리

## 권한
V1 목표: `activeTab`, `scripting`, `sidePanel`, `storage`.

## 동적 페이지
현재 DOM snapshot이 기준. 초기에는 무한 MutationObserver 대신 `다시 진단` 제공. V2에서 route change/limited observer 검토.

## iframe
V1 top frame 기본. cross-origin iframe은 미점검 범위로 표시.

## CSS background/canvas/SVG
`<img>` ALT 진단과 분리하며 V1 점수에 강제 포함하지 않는다.

## 전체 사이트
Extension 단독 crawler로 무리하게 구현하지 않는다. Deep Scan은 SearchTune API 또는 별도 backend/worker로 분리한다.
