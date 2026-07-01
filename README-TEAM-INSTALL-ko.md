# BEAI Knowledge Loop for Codex 팀 설치 안내

이 zip은 팀원이 자기 Codex 앱에 BEAI Knowledge Loop for Codex 플러그인을 설치해 볼 수 있도록 만든 내부 배포 후보입니다.

## 포함된 것

- Codex plugin manifest
- BEAI Knowledge Loop skill
- MCP server
- local marketplace file
- 설치 스크립트
- 안전 경계/제품 원칙/설치 문서

## 포함하지 않은 것

- 윤의 로컬 `.codex/knowledge-loop` 작업 기록
- BEAI Harness 내부 작업 로그
- 공개 릴리즈 선언
- 고객/계정/돈/계약/법률 관련 자동화

## 설치 방법

1. zip 파일을 원하는 폴더에 풉니다.
2. 풀린 폴더 안의 `설치.command`를 실행합니다.
3. Codex 앱을 재시작합니다.
4. Codex Plugins 화면에서 `BEAI Knowledge Loop for Codex`를 설치합니다.
5. 새 Codex 대화창에서 Knowledge Loop가 필요한 작업을 시작합니다.

## 작동 원칙

핵심 원칙:

> Auto-capture, not auto-approve.

자동으로 해도 되는 것:

- 과거 지식 검색
- brief 조회
- 작업 후 review-only 초안 기록
- review queue 조회

자동으로 하면 안 되는 것:

- durable memory 승격
- `approved` 확정
- 외부 발송
- 고객 응대
- 공개 게시
- 결제/계약/법률/계정/배포
- cron/hook/상시 자동화 활성화

## 설치 후 확인

설치 후 새 Codex 대화에서 다음처럼 요청해 볼 수 있습니다.

```text
BEAI Knowledge Loop를 사용해서 이 작업 전에 관련 과거 판단을 먼저 찾아줘.
```

작업이 끝난 뒤에는 Knowledge Loop가 review-only draft 후보를 남길 수 있습니다.

## 문제 해결

설치 스크립트가 실패하면 다음을 확인합니다.

- Node.js가 설치되어 있는가
- Codex CLI가 설치되어 있는가
- zip을 읽기 전용 위치가 아니라 일반 작업 폴더에 풀었는가
- Codex 앱을 재시작했는가

이 패키지는 내부 팀 검토용 후보입니다. 공개 배포판이나 고객용 설치 파일이 아닙니다.
