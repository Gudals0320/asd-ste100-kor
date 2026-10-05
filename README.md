# STE-KO Codex

AI가 한국어 글을 처음 작성할 때 참고하는 문서형 Codex 스킬이다. 독자가 적게 추측하도록 쓰되, 사실과 불확실성을 바꾸지 않는다.

설명문, 분석문, 업무 메시지, 보고서, 안내문과 절차문에 적용한다. 글의 목적과 독자에 맞춰 구조와 말투를 고른다. 모든 글을 짧게 만들거나 같은 형식에 맞추지 않는다.

## 스킬 구성

- [SKILL.md](skills/ste-ko-codex/SKILL.md): 작성 순서와 핵심 원칙
- [작성 규칙](skills/ste-ko-codex/references/writing-rules.md): 의미, 문장, 구조, 글 종류에 따른 판단
- [표현 선택](skills/ste-ko-codex/references/expression-choices.md): 문맥에 따른 어휘와 문법 선택
- [작성 예시](skills/ste-ko-codex/references/examples.md): 주어진 정보와 그 정보로 작성한 글

`skills/ste-ko-codex` 폴더 전체가 스킬 단위다. Codex에서 불러온 뒤 `$ste-ko-codex`와 작성 요청을 함께 지정한다. 관련 글쓰기 요청에는 자동으로 적용할 수 있지만, 단지 한국어로 대화한다는 이유로 모든 응답에 강제하지 않는다. 이 저장소를 가져오는 것만으로 현재 세션에 설치되지는 않는다.

예: `$ste-ko-codex 아래 정보를 바탕으로 처음 사용하는 사람에게 보낼 기능 안내문을 작성해줘.`

## 작성 방향

사실·조건·예외·부정·수치·확신 수준을 먼저 지킨다. 핵심 용어와 논리 관계를 명확히 하고, 근거가 없는 숫자나 원인을 만들지 않는다. 어절 수와 문장 수는 판단을 돕는 신호로만 쓴다. 자연스러운 문장, 유용한 비유와 표, 글의 목적에 맞는 전개를 허용한다.

## 출처

[beamonic/ste-ko](https://github.com/beamonic/ste-ko)의 파생 작업이다. 원본 기준 커밋과 변경 방향은 [ORIGIN.md](ORIGIN.md)에 기록한다. ASD-STE100의 공식 번역이나 준수 인증을 표방하지 않는다. 원본의 MIT 저작권 고지는 [LICENSE](LICENSE)에 유지한다.
