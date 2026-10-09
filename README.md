# 디지털 교수·학습 연구 에이전트 작업공간

두 전문 에이전트와 여러 연구 프로젝트를 분리해 관리하는 작업공간입니다.

```text
research-proposal-agent/
├─ AGENTS.md
├─ README.md
├─ agents/
│  ├─ research-design/
│  │  ├─ AGENTS.md
│  │  ├─ README.md
│  │  ├─ templates/
│  │  └─ references/
│  └─ literature-search/
│     └─ AGENTS.md
└─ projects/
   ├─ README.md
   └─ _template/
```

## 에이전트

| 폴더 | 역할 |
| --- | --- |
| `agents/research-design/` | 좋은 연구보고서 작성을 위한 연구문제 추천, 사용자 선택 후 연구설계·연구계획서 Markdown/DOCX·논리와 근거 점검 |
| `agents/literature-search/` | 연구보고서의 근거 공백을 분석하고 핵심 문헌의 서지정보와 공개 원문 PDF를 검증·저장 |

루트 `AGENTS.md`는 사용자 요청에 맞는 전문 에이전트 지침을 선택하는 라우터입니다. 실제 역할 규칙은 각 에이전트 폴더의 `AGENTS.md`에서 독립적으로 관리합니다.

현행 사용법과 변경 비교는 `agents/research-design/README.md`에 있습니다. 연구 산출물 경로 `outputs/research-proposal/`은 두 에이전트가 함께 사용합니다.

## 프로젝트

연구별 자료는 `projects/<project-name>/` 아래에 둡니다. 새 연구 아이디어를 제시하면 에이전트가 핵심 문제를 요약한 이름을 자동으로 정하고 `projects/_template/`의 구조를 복사해 바로 시작합니다. 프로젝트 이름이나 폴더 생성 허락을 별도로 묻지 않습니다. 사용자가 이름이나 경로를 지정하면 그 지정을 우선합니다.

```text
projects/<project-name>/
├─ inputs/user-provided/
├─ outputs/
│  ├─ research-proposal/
│  │  ├─ recommendations/
│  │  ├─ drafts/
│  │  ├─ final/
│  │  ├─ reviews/
│  │  └─ handoff/
│  └─ literature/
└─ literature/
   ├─ pdfs/
   └─ quarantine/
```

프로젝트명과 파일명에는 학생·교사·학교를 식별할 수 있는 정보를 넣지 않습니다.

학교급·학년·교과를 따로 입력하지 않으면 **중학교 사회**의 공통 수준을 기본값으로 사용합니다. 세부 학년은 미지정으로 표시하며 기본값 확인 질문 없이 진행합니다. 사용자가 특정 학교급·학년·교과를 제공하면 해당 항목은 그 입력을 우선하고, 학년별 단원·성취기준은 실제 입력이 있을 때 구체화합니다. 기간·인원·기기 등은 별도의 가정 또는 확인 사항으로 남깁니다.

## 기본 작업 순서

1. 새 아이디어를 제시하면 에이전트가 `_template` 구조를 복사해 연구 프로젝트 폴더를 자동으로 만들고 이름과 경로를 안내합니다. 같은 이름이 있으면 번호를 붙여 구분합니다.
2. 수업안, 활동지, 평가도구 등 익명화한 자료를 `inputs/user-provided/`에 둡니다.
3. 연구설계 에이전트가 연구문제를 추천합니다. 사용자가 선택하면 필요한 질문 후 연구설계·계획서 Markdown/DOCX·논리와 근거 점검을 수행합니다. 계획서 초안은 `drafts/`에, 추천·점검·인계 문서는 각각 별도 폴더에 둡니다.
4. 문헌 검색은 요청할 때만 수행합니다. 연구계획서 Markdown의 정확한 경로와 근거 공백을 입력으로 지정해 핵심 문헌을 선별합니다.
5. 문헌 검토 결과는 `<project>/outputs/literature/`, 검증한 공개 원문 PDF는 `<project>/literature/pdfs/`에 저장합니다.
6. 문헌을 보고서에 반영하는 작업은 사용자가 별도로 요청할 때 수행합니다.

`_template`은 실제 연구 프로젝트가 아닙니다. 새 아이디어는 새 프로젝트에서 시작하며, 현재 연구의 후속 작업은 선택한 프로젝트에서 이어갑니다. 연구설계에 필요한 질문에는 가정과 미확인 사항을 표시하면서 초안 작업을 병행합니다. 계획서의 기대 변화는 실제 연구결과로 작성하지 않으며, 검색 전 근거가 필요한 곳에는 `[근거 필요]` 표시를 남깁니다.

유료벽, 로그인 제한, CAPTCHA 또는 기술적 보호조치는 우회하지 않습니다. 공개 PDF를 확보하지 못한 문헌은 공식 URL과 접근 상태만 기록합니다.
