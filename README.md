# FinAgent config-repo

Backend의 Config Server가 읽는 설정 파일 저장소입니다. 담당: 클라우드 곽호윤. 서비스 코드는 [Backend](https://github.com/cnsFinalProject/Backend) 레포에 있습니다.

## 파일 규칙

파일 이름은 `서비스이름-프로필.yml`로 씁니다. `backend.yml`은 모든 프로필 공통, `backend-dev.yml`은 dev 프로필에서만 쓰입니다. 서비스가 정해지면 파일을 추가합니다.

| 파일 | 용도 |
| --- | --- |
| `examples/*.yml.example` | 키 이름만 있는 예시. 실제 값 없음 |

DB 비밀번호, LLM API 키, JWT 키 같은 값은 평문으로 올리지 않습니다. Config Server 암호화로 `{cipher}` 값을 만들어 넣거나 환경 변수로 넘깁니다.

LLM·Vector DB처럼 아직 정하지 않은 구성은 `finagent.llm.provider` 같은 키로 구현체를 고르게 두어, 결정이 바뀌어도 설정만 바꾸면 되게 합니다.

## 브랜치

Config Server가 `main`을 읽기 때문에 이 레포는 `main` 하나만 씁니다. 설정을 바꿀 때도 이슈 번호로 브랜치를 만들어 PR로 합칩니다. 나머지 규칙은 Backend 레포의 [협업규칙.md](https://github.com/cnsFinalProject/Backend/blob/develop/docs/협업규칙.md)를 따릅니다.
