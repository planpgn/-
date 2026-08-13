# Security & Privacy

## Local-first
기본 Scan은 브라우저 내부에서 끝낸다. 외부 전송 없이 가능한 규칙은 모두 로컬 처리한다.

## 권한 최소화
- broad `<all_urls>` 기본 요구 금지
- 사용자 액션 기반 `activeTab`
- 필요 시 `scripting`, `sidePanel`, `storage`
- Deep Scan은 optional permission 또는 별도 backend 검토

## AI 기능
V2의 AI ALT 제안은 명시적 사용자 액션일 때만 호출한다. 전송 전 선택 이미지, 상품명/H1, 주변 텍스트, brand/category 등 전송 범위를 표시한다.

## API Key
- extension bundle에 secret 하드코딩 금지
- 상용 배포는 `extension -> controlled backend -> AI API` 권장

## 데이터 최소화
- URL query/hash는 report에서 제거/마스킹
- 입력폼/비밀번호/결제/회원정보 값 수집 금지
- scan history는 요약 데이터 중심

## 공개 배포
Chrome Web Store 배포 전 실제 권한과 데이터 사용 정책을 재점검한다. 개발 편의 권한을 그대로 상용 배포하지 않는다.
