# 디지털 교수·학습 연구 에이전트 작업공간

두 전문 에이전트와 여러 연구 프로젝트를 분리해 관리하는 작업공간입니다.

```text
research-proposal-agent/
├─ AGENTS.md
├─ README.md
├─ agents/
│  ├─ research-proposal/
│  │  ├─ AGENTS.md
│  │  ├─ templates/
│  │  ├─ examples/
│  │  └─ tests/
│  └─ literature-search/
│     └─ AGENTS.md
└─ projects/
   ├─ README.md
   └─ _template/
```

## 에이전트

| 폴더 | 역할 |
| --- | --- |
| `agents/research-proposal/` | 수업 문제를 연구주제, 연구문제, 교수·학습 전략, 평가계획 및 연구보고서로 발전 |
| `agents/literature-search/` | 연구보고서의 근거 공백을 분석하고 핵심 문헌의 서지정보와 공개 원문 PDF를 검증·저장 |

루트 `AGENTS.md`는 사용자 요청에 맞는 전문 에이전트 지침을 선택하는 라우터입니다. 실제 역할 규칙은 각 에이전트 폴더의 `AGENTS.md`에서 독립적으로 관리합니다.

## 프로젝트

연구별 자료는 `projects/<project-name>/` 아래에 둡니다. 새 연구는 `projects/_template/`의 구조를 복사해 시작합니다.

```text
projects/<project-name>/
├─ inputs/user-provided/
├─ outputs/
│  ├─ research-proposal/
│  │  ├─ drafts/
│  │  └─ final/
│  └─ literature/
└─ literature/
   ├─ pdfs/
   └─ quarantine/
```

프로젝트명과 파일명에는 학생·교사·학교를 식별할 수 있는 정보를 넣지 않습니다.

## 기본 작업 순서

1. `_template` 구조를 복사해 연구 프로젝트 폴더를 만듭니다.
2. 수업안, 활동지, 평가도구 등 익명화한 자료를 `inputs/user-provided/`에 둡니다.
3. 연구보고서 에이전트가 초안 또는 최종 보고서를 `<project>/outputs/research-proposal/`에 작성합니다.
4. 문헌 검색 에이전트가 해당 보고서를 입력으로 핵심 문헌을 선별합니다.
5. 문헌 검토 결과는 `<project>/outputs/literature/`, 검증한 공개 원문 PDF는 `<project>/literature/pdfs/`에 저장합니다.
6. 문헌을 보고서에 반영하는 작업은 사용자가 별도로 요청할 때 수행합니다.

유료벽, 로그인 제한, CAPTCHA 또는 기술적 보호조치는 우회하지 않습니다. 공개 PDF를 확보하지 못한 문헌은 공식 URL과 접근 상태만 기록합니다.
