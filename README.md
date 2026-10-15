# ASD-STE100 참고 한국어 글쓰기

ASD-STE100(Simplified Technical English)의 명확한 기술 문서 작성 원칙을 참고한 한국어 글쓰기용 AI 스킬이다. AI가 한국어 초안을 작성할 때 용어와 논리 관계를 명확히 표현하고, 사실과 불확실성을 보존하도록 돕는다.

설명문, 분석문, 업무 메시지, 보고서, 안내문과 절차문에 적용한다. 글의 목적과 독자에 맞춰 구조와 말투를 고른다. 모든 글을 짧게 만들거나 같은 형식에 맞추지 않는다.

같은 철학과 작성 순서를 두 가지 도구용으로 제공한다.

| 스킬 | 대상 도구 | 위치 |
|---|---|---|
| `ste-ko-codex` | OpenAI Codex | [skills/ste-ko-codex](skills/ste-ko-codex) |
| `ste-ko-claude` | Claude Code, Claude 앱, Claude Agent SDK | [skills/ste-ko-claude](skills/ste-ko-claude) |

두 스킬의 참고 문서(작성 규칙, 표현 선택, 작성 예시)는 내용이 같다. 각 폴더가 독립적으로 설치되도록 파일을 따로 두었으므로, 규칙을 고칠 때는 두 폴더를 함께 고친다.

## 스킬 구성

각 스킬 폴더는 같은 구조를 가진다.

- `SKILL.md`: 작성 순서와 핵심 원칙. 도구별 설명(frontmatter)과 호출 방식만 다르다.
- `references/writing-rules.md`: 의미, 문장, 구조, 글 종류에 따른 판단
- `references/expression-choices.md`: 문맥에 따른 어휘와 문법 선택
- `references/examples.md`: 주어진 정보와 그 정보로 작성한 글

Codex용 폴더에는 Codex 인터페이스 정보인 `agents/openai.yaml`이 추가로 있다. Claude용 폴더에는 이에 해당하는 파일이 없고, `SKILL.md`의 frontmatter가 그 역할을 한다.

## Codex에서 사용

`skills/ste-ko-codex` 폴더 전체가 스킬 단위다. Codex에서 불러온 뒤 `$ste-ko-codex`와 작성 요청을 함께 지정한다.

예: `$ste-ko-codex 아래 정보를 바탕으로 처음 사용하는 사람에게 보낼 기능 안내문을 작성해줘.`

## Claude에서 사용

`skills/ste-ko-claude` 폴더 전체가 스킬 단위다. 이 저장소를 가져오는 것만으로 설치되지는 않으므로, 폴더를 Claude가 스킬을 읽는 위치에 둔다.

- Claude Code, 개인용: `~/.claude/skills/ste-ko-claude/`에 폴더를 복사한다.
- Claude Code, 프로젝트용: 프로젝트의 `.claude/skills/ste-ko-claude/`에 폴더를 복사한다.
- Claude 앱: 폴더를 zip으로 압축해 설정의 스킬 항목에 올린다. 압축 파일 안에 `ste-ko-claude/SKILL.md`가 있어야 한다.

설치 후 `/ste-ko-claude` 뒤에 작성 요청을 적는다. 관련 글쓰기 요청에는 Claude가 설명을 보고 자동으로 적용할 수 있지만, 단지 한국어로 대화한다는 이유로 모든 응답에 강제하지 않는다.

예: `/ste-ko-claude 아래 정보를 바탕으로 처음 사용하는 사람에게 보낼 기능 안내문을 작성해줘.`

## 작성 방향

사실·조건·예외·부정·수치·확신 수준을 먼저 지킨다. 핵심 용어와 논리 관계를 명확히 하고, 근거가 없는 숫자나 원인을 만들지 않는다. 어절 수와 문장 수는 판단을 돕는 신호로만 쓴다. 자연스러운 문장, 유용한 비유와 표, 글의 목적에 맞는 전개를 허용한다.

## 참고 표준

[ASD-STE100 공식 웹사이트](https://www.asd-ste100.org/)를 참고한다. 용어를 일관되게 사용하고 문장과 절차를 명확히 구성하는 방향을 한국어 글쓰기에 활용한다. 영어 전용 어휘와 문법 제한을 한국어에 그대로 적용하지 않는다.

이 스킬은 ASD-STE100의 공식 번역이나 인증된 구현이 아니다.

## 라이선스

[MIT License](LICENSE)를 따른다.
