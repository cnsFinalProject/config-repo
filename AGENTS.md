# AGENTS.md — FinAgent config-repo AI 작업 가이드

## 규칙
- 이 레포는 Config Server 설정 전용이다. 코드를 넣지 않는다.
- 파일 이름: `서비스이름-프로필.yml` (예: `backend-dev.yml`).
- **비밀 값(DB 비밀번호, LLM API 키, JWT 키)을 평문으로 쓰지 않는다.** `{cipher}...` 또는 `${ENV_NAME}` 참조만 쓴다. 평문 비밀 값을 발견하면 작업을 멈추고 사용자에게 알린다.
- 미정 구성(LLM, Vector DB, RDB)은 값 대신 선택 키로 둔다. 예: `finagent.llm.provider: ${LLM_PROVIDER:TODO}`.
- 브랜치는 `main` 하나. 수정은 `chore/WBS번호-작업명` 브랜치 → PR → `main`.
- 기획 기준: [project-context.md](https://github.com/cnsFinalProject/Backend/blob/develop/docs/project-context.md), 협업 규칙: [협업규칙.md](https://github.com/cnsFinalProject/Backend/blob/develop/docs/협업규칙.md).
