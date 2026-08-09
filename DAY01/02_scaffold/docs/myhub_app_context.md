# MyHub Technical Context — ① 스캐폴딩 시작

- **B/E**
    - 언어: Python
    - 웹 프레임워크: FastAPI + uvicorn (`:8080`)
    - DB 접속: Supabase PostgreSQL · session pooler
    - DB 드라이버: psycopg (동기 호출)
    - 계약: Pydantic DTO
- **F/E**
    - 언어: TypeScript
    - UI: React + React Router
    - 빌드 · 개발 서버: Vite (`:5173`, `/api` 프록시)
    - API 호출 및 타입: `openapi-fetch` + `openapi-typescript`
- **DBMS**
    - 엔진: Supabase PostgreSQL

- **공통사항**
    - 라이브러리/패키지의 버전은 의도치 않은 버전 충돌을 피하기 위해 의도적으로 명시하지 않음 (자동 최신버전 사용)

---

## 프로젝트 생성 전에 정해둘 것

- Supabase Security: Data API **켬** / 새 테이블 자동 노출 **끔** / 자동 RLS **켬**
- Region: Seoul 또는 Tokyo
- Database Password: 영문자 + 숫자만 (생성 후 다시 못 봄)
- 비밀값은 `.env`(커밋하지 않음), `.env.example` 파일로 내용 가이드
