# CNS Final Project Config Repo

환경별 설정을 관리할 초기 구조입니다. Config Server나 실행 중인 서비스와의 연결은 아직 구성하지 않았습니다.

## 파일 구조
| 파일 | 용도 |
| --- | --- |
| `examples/application.yml.example` | 공통 설정 작성 예 |
| `examples/backend.yml.example` | 백엔드 공통 설정 예 |
| `examples/backend-local.yml.example` | 로컬 환경 설정 예 |
| `examples/backend-dev.yml.example` | 개발 환경 설정 예 |
| `examples/backend-prod.yml.example` | 운영 환경 설정 예 |
| `.env.example` | 필요한 환경변수 이름과 로컬 예시 |

`.example` 파일은 문서용입니다. 현재 자동으로 읽히거나 배포되지 않습니다.
Spring Cloud Config를 채택하면 `spring.application.name`에 맞는 파일명과
프로필을 확정한 뒤 실제 설정으로 옮기고 [Backend](https://github.com/cnsFinalProject/Backend)에 연결 방법을 기록합니다.
다른 설정 도구를 선택하면 파일 형식을 해당 도구에 맞춥니다.

## 비밀값 관리
비밀번호·토큰·API 키는 실제 값 대신 환경변수 참조를 사용합니다.
운영 비밀값은 배포 환경의 비밀 저장소에 보관하고 `.env`는 커밋하지 않습니다.
현재 자동 비밀값 검사나 설정 배포 CI는 구성하지 않았습니다.

## 설정 변경 절차
이슈에 목적·영향을 작성하고 PR에서 검토합니다. 적용·재시작·롤백 방법은
실제 실행 환경이 정해지면 [platform](https://github.com/cnsFinalProject/platform)에 기록합니다.
