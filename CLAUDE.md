# 가격표 카탈로그 — 카탈로그 에이전트

> **소속 부서**: 영업부 — 거래처 가격표 제공
> **상위 문서**: ../CLAUDE.md (ERP 총괄)

## 역할
Supabase `products` 테이블 데이터를 가격표 카탈로그 형태로 표시하는 Next.js 사이트 관리.

## 기술 스택
- Next.js 14 + TypeScript + Tailwind CSS
- Supabase JS v2 (데이터 조회)
- 정적 빌드 (`next export` → `out/`)

## 배포
- GitHub: `yeocheon2024-droid/product-catalog-price`
- URL: product-catalog-price.pages.dev
- 호스팅: Cloudflare Pages (자체 빌드)

## 주요 기능
- 품목 카탈로그 그리드/리스트 뷰
- 가격 표시 모드 (`?price=on` 쿼리 파라미터)
- 카테고리 필터 (대분류/중분류)
- 무한 스크롤
- 쌀 카테고리: 가격 오름차순 정렬

## 환경변수
```
NEXT_PUBLIC_SUPABASE_URL=...
NEXT_PUBLIC_SUPABASE_ANON_KEY=...
```

## 규칙
1. Supabase anon key 외 API 키 코드 내장 금지
2. 빌드: `npm run build` → `out/` 생성 확인
3. 이미지 로딩 실패 시 로고 fallback 필수
