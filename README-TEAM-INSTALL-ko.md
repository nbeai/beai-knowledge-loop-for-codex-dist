# BEAI Knowledge Loop for Codex 팀 설치 안내

이 zip은 팀원이 자기 Codex 앱에 BEAI Knowledge Loop for Codex 플러그인을 설치해 볼 수 있도록 만든 production-candidate 배포 파일입니다.

## 포함된 것

- Codex plugin manifest
- BEAI Knowledge Loop skill
- MCP server
- local marketplace file
- 설치 스크립트
- 설치 루트 검증 스크립트
- package hygiene 검사
- 안전 경계/제품 원칙/설치 문서

## 포함하지 않은 것

- 개발자의 로컬 `.codex/knowledge-loop` 작업 기록
- BEAI Harness 내부 작업 로그
- durable memory promotion
- 고객/계정/돈/계약/법률 관련 자동화
- cron/hook/상시 자동화 활성화

## 설치 방법

1. zip 파일을 원하는 일반 작업 폴더에 풉니다.
2. 풀린 폴더 안의 `설치.command`를 실행합니다.
3. 설치 스크립트가 manifest의 MCP 경로를 현재 설치 폴더 기준으로 패치하고 검증합니다.
4. Codex 앱을 완전히 재시작합니다.
5. Codex Plugins 화면에서 `BEAI Knowledge Loop for Codex`를 설치합니다.
6. 새 Codex 대화창에서 Knowledge Loop가 필요한 작업을 시작합니다.

## 설치 후 상태 구분

- package unpacked: zip을 푼 상태
- marketplace added: Codex에 local marketplace가 추가된 상태
- plugin installed: Codex Plugins에서 추가한 상태
- mcp path verified: 설치 루트 안의 MCP server를 가리키는 상태
- new thread active: 새 대화창에서 skill/MCP가 사용 가능한 상태

기존 대화창에는 plugin/MCP hot reload가 즉시 반영되지 않을 수 있습니다. 적용 확인은 새 대화창 기준으로 합니다.

## 작동 원칙

핵심 원칙:

> Auto-capture, not auto-approve.

자동으로 해도 되는 것:

- 과거 지식 검색
- brief 조회
- 작업 후 review-only 초안 기록
- review queue 조회
- retrieval eval 실행

자동으로 하면 안 되는 것:

- durable memory 승격
- `approved` 확정
- 외부 발송
- 고객 응대
- 공개 게시
- 결제/계약/법률/계정/배포
- cron/hook/상시 자동화 활성화

## 문제 해결

설치 스크립트가 실패하면 다음을 확인합니다.

- Node.js가 설치되어 있는가
- Codex CLI가 설치되어 있는가
- zip을 읽기 전용 위치가 아니라 일반 작업 폴더에 풀었는가
- `__RUN_INSTALL_COMMAND_FIRST__` placeholder가 설치 후에도 남아 있지는 않은가
- MCP server path가 plugin install root 안쪽을 가리키는가
- Codex 앱을 완전히 재시작했는가

이 패키지는 production-candidate입니다. 실사용자 반응과 외부 감사 전에는 stable release로 표현하지 않습니다.
