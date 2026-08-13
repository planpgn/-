# Audit Rules

## 원칙
진단은 `사실 -> 판정 -> 설명 -> 조치` 순서. 검색/광고 성과를 보장하지 않는다.

## Image ALT
- `IMG_ALT_MISSING` Critical: alt attribute 자체가 없음. 단 presentation/decoration 역할은 예외 검토.
- `IMG_ALT_EMPTY_REVIEW` Warning/Info: `alt=""`. 장식용이면 정상일 수 있어 무조건 실패 금지.
- `IMG_ALT_FILENAME` Warning: ALT가 `detail_1-1.jpg`, `/images/product01.png`처럼 파일명/경로와 사실상 동일.
- `IMG_ALT_GENERIC` Warning: `image`, `img`, `photo`, `이미지`, `사진`, `상품이미지`, `상세페이지` 등 지나치게 일반적.
- `IMG_ALT_DUPLICATE` Warning: 동일 non-empty ALT 반복. 정상 썸네일 가능성이 있어 검토형으로 표시.
- `IMG_BROKEN` Critical: 렌더링 실패 이미지.

## Metadata
- `META_TITLE_MISSING`
- `META_DESCRIPTION_MISSING`
- `H1_MISSING`
- `H1_MULTIPLE_REVIEW`
- `CANONICAL_MISSING_REVIEW`
- `OG_TITLE_MISSING_REVIEW`
- `OG_DESCRIPTION_MISSING_REVIEW`

길이 기준은 경험칙으로만 표시하고 공식 규칙처럼 단정하지 않는다.

## JSON-LD / Schema
- `SCHEMA_JSON_INVALID` Critical: JSON-LD parse 실패.
- `SCHEMA_PRODUCT_MISSING` Warning: 상품 상세로 높은 확률인데 Product schema 없음.

Product entity가 존재하면 `@type`, `name`, `description`, `image`, `brand`, `offers`, `offers.price`, `offers.priceCurrency`를 점검한다. `aggregateRating`은 실제 페이지에 리뷰/평점이 있을 때만 점검한다. 허위 값 생성 금지.

## Content
- product/brand name이 visible text에 있는지
- H1/H2 구조
- 핵심 상품 설명 텍스트
- CTA label

V1에서 LLM으로 콘텐츠 품질 자동 판정 금지.

## Consistency
가능할 때 visible product name/price/brand와 schema의 name/Offer price/brand를 normalization 후 비교한다. 확정 오류가 아니라 `검토 필요`로 표현한다.

## Selector
id/data attribute/semantic relation 우선. DOM 순서에만 의존하는 brittle selector를 단독 저장하지 않는다.
