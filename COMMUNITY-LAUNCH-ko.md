# BEAI Knowledge Loop 커뮤니티 게시 원고

이 문서는 커뮤니티별 게시용 초안이다. 같은 글을 복붙하지 말고, 채널 성격에 맞춰 아래 버전 중 하나를 사용한다.

## 공통 한 줄

Codex도 Claude Code도 Cursor도 결국 LLM입니다. 그래서 더 큰 자동 기억보다 중요한 것은, 사람이 승인할 수 있는 작업 기억 루프라고 봅니다.

## ClawHub

제목:

```text
BEAI Knowledge Loop for Codex: AI 에이전트를 위한 review-first 작업 기억 루프
```

본문:

```text
AI coding agent는 점점 강해지고 있습니다. 하지만 Codex, Claude Code, Cursor도 결국 LLM 기반 작업자입니다.

문제는 단순히 "AI에게 더 많은 문서를 읽히는 것"이 아니라고 봅니다. AI가 일하면서 만든 판단, 실수, 근거, 다음 행동이 사람의 승인 가능한 지식 후보로 남아야 합니다.

BEAI Knowledge Loop for Codex는 이 관점에서 만든 Codex용 public preview 패키지입니다.

- 작업 전: 과거 판단과 근거를 검색합니다.
- 작업 중: 기존 결정과 위험 경계를 참고합니다.
- 작업 후: review-only 지식 후보를 남깁니다.
- 승인 전: durable memory나 외부 행동으로 승격하지 않습니다.

핵심 원칙은 Auto-capture, not auto-approve 입니다.

LLM Wiki가 AI가 읽는 도서관이라면, Knowledge Loop는 AI 직원의 업무일지와 인수인계 체계에 가깝습니다.

GitHub:
https://github.com/nbeai/beai-knowledge-loop-for-codex-dist
```

## GeekNews

제목:

```text
Show GN: Codex용 review-first 작업 기억 루프를 만들었습니다
```

본문:

```text
Codex 작업을 하다 보면 세션마다 같은 판단을 다시 설명하거나, 이전에 발견한 함정이 다음 작업에 반영되지 않는 문제가 생깁니다.

BEAI Knowledge Loop for Codex는 이 문제를 "자동 메모리"가 아니라 "review-first 작업 기억 루프"로 풀어보는 실험입니다.

구조는 단순합니다.

1. 작업 전에 knowledge.search로 과거 판단을 찾습니다.
2. 필요한 기록은 brief로 요약합니다.
3. 작업 후 capture_draft로 review-only 기록을 남깁니다.
4. 사람이 확인한 것만 approved 지식으로 봅니다.

중요한 점은 자동 승인하지 않는다는 것입니다. 외부 발송, 공개 게시, 고객 응대, 결제/계약/법률/계정/배포 같은 작업은 여전히 사람 승인 경계로 둡니다.

현재는 Codex용 public preview / team install candidate입니다.

GitHub:
https://github.com/nbeai/beai-knowledge-loop-for-codex-dist
```

## Disquiet

제목:

```text
AI 에이전트가 일한 흔적을 지식 자산으로 남기는 BEAI Knowledge Loop
```

본문:

```text
BEAI Knowledge Loop는 AI 에이전트와 반복적으로 일하는 사람을 위한 작업 기억 시스템입니다.

많은 AI memory 접근은 "AI에게 더 많은 맥락을 넣자"에 집중합니다. 저는 반대로 "사람이 승인할 수 있는 판단만 조직의 지식이 되게 하자"는 쪽이 더 중요하다고 봤습니다.

그래서 BEAI Knowledge Loop는 자동 메모리가 아니라 review-first 루프입니다.

- AI가 작업 전 과거 결정을 찾고
- 작업 후 판단/근거/함정/다음 행동을 후보로 남기며
- 사람 승인 전에는 durable memory로 승격하지 않습니다

첫 구현은 Codex용 plugin + MCP tool + local knowledge store 구조입니다.

GitHub:
https://github.com/nbeai/beai-knowledge-loop-for-codex-dist
```

## OKKY

제목:

```text
Codex/Claude Code/Cursor 같은 AI coding agent에 작업 기억 루프가 필요하다고 느꼈습니다
```

본문:

```text
AI coding agent를 쓰다 보면 생산성은 올라가지만, 세션 간 판단이 계속 끊기는 문제가 있습니다.

그래서 Codex용으로 BEAI Knowledge Loop라는 public preview를 만들어봤습니다.

목표는 자동 메모리가 아닙니다. 오히려 반대입니다.

- AI가 과거 판단을 먼저 찾게 하고
- 작업 후에는 review-only draft만 남기고
- 사람이 확인한 것만 approved로 올리는 구조입니다.

LLM Wiki나 RAG처럼 "읽기 좋은 지식창고"를 만드는 것과 달리, AI 작업자의 업무일지/인수인계/승인 대기열에 더 가깝습니다.

혹시 Codex, Claude Code, Cursor를 오래 쓰시는 분들은 이런 문제가 있었는지 궁금합니다.

GitHub:
https://github.com/nbeai/beai-knowledge-loop-for-codex-dist
```

## Velog / 기술 블로그

제목:

```text
Codex도 결국 LLM이다: AI coding agent를 위한 작업 기억 루프 설계
```

요지:

```text
1. AI coding agent는 강하지만 세션 간 작업 기억이 약하다.
2. 자동 memory write는 편하지만 위험하다.
3. 그래서 review-first 구조가 필요하다.
4. BEAI Knowledge Loop는 Skill, MCP Tool, local JSON store로 구성된다.
5. 핵심 원칙은 Auto-capture, not auto-approve.
6. LLM Wiki와 다른 점은 "읽기 좋은 지식창고"가 아니라 "AI 작업자의 업무일지와 승인 대기열"이라는 점이다.
```

## Brunch / 칼럼

제목:

```text
AI 에이전트도 결국 LLM이다
```

요지:

```text
AI 도구가 강해질수록 사람은 더 뒤로 물러나도 된다고 생각하기 쉽다. 그러나 Codex, Claude Code, Cursor도 결국 LLM 기반 작업자다. 이 말은 그들이 쓸모없다는 뜻이 아니라, 그들이 일한 흔적을 사람의 판단 체계 안으로 가져와야 한다는 뜻이다.

다음 단계의 AI 업무 환경은 더 큰 자동 기억이 아니라, 사람이 승인할 수 있는 작업 기억 루프 위에서 만들어질 가능성이 크다.
```

## 작성자 표기

```text
Created by BEAI.
Copyright (c) 2026 박종윤 / Jongyoon Park (@aigis0927).
GitHub: https://github.com/nbeai
```

