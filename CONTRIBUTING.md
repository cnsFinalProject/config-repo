# 개발 가이드

브랜치, 커밋, PR, 리뷰 규칙은 Backend 레포의 [협업규칙.md](https://github.com/cnsFinalProject/Backend/blob/develop/docs/협업규칙.md) 하나로 관리합니다. 요약:

- 이슈 1개 = WBS 작업 1개 = 담당 1명, 제목 `[2.3.1] 작업명`
- 브랜치 `feat/2.3.1-cashflow-api` (develop에서 분기)
- 커밋 `[Add]_2.3.1/CashflowApi` + `- 변경 내용`
- PR은 develop 대상, 본문에 `Closes #이슈번호`, 승인 1개 이상
- 기획이 바뀌면 "기획·설계 결정" 이슈 → project-context.md 갱신
