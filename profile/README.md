<div align="center">

# Workly

### 팀의 대화를 실행 가능한 업무로 연결하는 프로젝트 협업 플랫폼

워크스페이스에서 프로젝트와 팀을 관리하고, 실시간 대화와 AI 기반 Task 제안을 통해
기획부터 실행까지 이어지는 협업 흐름을 제공합니다.

[Front](https://github.com/Workly-Ai-Agent/Front) · [Back](https://github.com/Workly-Ai-Agent/Back) · [AI-Agent](https://github.com/Workly-Ai-Agent/AI-Agent) · [Test](https://github.com/Workly-Ai-Agent/Test)

</div>

---

## 프로젝트 소개

프로젝트 계획, 담당자, 진행 상황과 팀 대화를 하나의 협업 공간에 모읍니다. AI는 계획과 대화에서 실행 가능한 Task 및 담당자 제안을 만들고, 프로젝트 Leader가 검토하고 승인한 뒤 실제 업무에 반영합니다.

## 주요 기능

- **워크스페이스와 프로젝트 관리** — 팀 공간을 만들고 구성원, 프로젝트, 프로젝트 리더를 관리합니다.
- **Task 관리** — 담당자, 우선순위, 일정, 상태와 선행 업무를 확인하고 칸반 보드에서 진행 상태를 관리합니다.
- **실시간 협업 채팅** — 워크스페이스 및 프로젝트 대화로 팀의 논의를 이어갑니다.
- **AI 계획 제안** — 프로젝트 계획을 실행 가능한 Task와 담당자 추천으로 구조화합니다.
- **채팅 기반 Task 반영** — 대화에서 나온 새 업무나 기존 Task 변경을 제안으로 만들고, 승인 후 반영합니다.
- **사람이 검토하는 승인 흐름** — AI 제안을 자동 적용하지 않고 리더가 승인하거나 거절합니다.
- **스킬 관리** — 구성원이 스킬을 등록하고 프로필에서 스킬 후보를 추출할 수 있습니다.

## 협업 흐름

```text
워크스페이스 생성
       ↓
프로젝트 및 팀 구성
       ↓
계획 입력 또는 팀 채팅
       ↓
AI가 Task와 담당자를 제안
       ↓
리더가 검토하고 승인
       ↓
Task Board에서 실행 상황 관리
```

전체 계획을 세우거나 크게 바꿀 때는 전체 계획 제안을 사용하고, 팀 대화 중 생긴 개별 업무 추가·수정은 해당 채팅 메시지에서 제안합니다.

## 시스템 구성

| 구성 요소 | 기술 | 역할 |
| --- | --- | --- |
| [Front](https://github.com/Workly-Ai-Agent/Front) | React, TypeScript, Vite | 프로젝트, Task, 채팅 사용자 화면 |
| [Back](https://github.com/Workly-Ai-Agent/Back) | Kotlin, Spring Boot, Spring Data JPA | 인증, 권한, API, 데이터 저장, WebSocket |
| [AI-Agent](https://github.com/Workly-Ai-Agent/AI-Agent) | Python, FastAPI, LangChain, LangGraph | 계획 구성, 담당자 추천, 검증, 메시지 분류, 스킬 추출 |
| Database | H2 / PostgreSQL | 사용자, 워크스페이스, 프로젝트, Task, 채팅, 제안 저장 |

```text
React Frontend ── HTTP API / WebSocket ── Kotlin Spring Backend
                                                ├── H2 / PostgreSQL
                                                └── HTTP ── Python AI Agent
```

## 개발 안내

각 저장소의 README에서 실행 방법과 환경 변수 설정을 확인할 수 있습니다. AI 제안 기능을 사용하려면 AI Agent와 모델 API 키를 설정해야 합니다. 테스트 시나리오 도구는 [Test 저장소](https://github.com/Workly-Ai-Agent/Test)를 참고하세요.

## 팀

**Workly 개발팀**
