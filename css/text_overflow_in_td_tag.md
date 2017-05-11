# td태그에서 영문 텍스트 넘침 해결 방법

## 문제점 발견
td태그에 긴 영문텍스트를 삽입 했더니 텍스트 일부가 td공간을 벗어나 버림. 나는 텍스트를 강제로 줄바꿈 시키고 싶음.

## 문제점 탐구
- td태그 안에서의 문장은 `공백`을 기준으로 잘림.
- 내가 td태그에 삽입하고자 했던 텍스트는 `Graduation thesis`였음. 그런데 나의 테이블 가로 cell이 무려 11개였음.
- 셀의 가로 넓이가 좁아서 `Graduation`의 `on`이 바로 옆 셀을 침범하는 현상 발생.
- 물론 <table>태그에 `table-layout:fixed` 속성을 제거해 주면 `Graduation`은 옆에 셀을 침범하지 않음.
- 그런데 `table-layout:fixed` 속성을 제거할 경우 나의 테이블 넓이는 900px인데 td태그 안에 문장들이 공백을 기준으로 잘리면서 테이블 넓이가 900px를 넘어감.

## 해결방법
td태그에 `word-break:break-all` 속성 및 속성값을 사용하면 됨.

참조로 본 사이트에서 파이어폭스에서는 `word-break`속성이 지원되지 않는다고 했는데 최신버전에서는 되는지 테스트결과 된다.

### word-break 속성값
| Value | Description |
| --- | --- |
| normal | 기본값. 일반적인 규칙에 따라 줄바꿈 함.|
| break-all | 문자를 강제로 줄바꿈. 아시아 언어(CJK)에서는 normal처럼 행동하며 비 아시아 언어에 사용할 때는 임의대로 줄바꿈 함. *CJK는 chinese, Japanese, Korean의 약자.|
| keep-all  | 문자쌍 사이의 줄바꿈이 금지.|

한글의 경우 word-break 의 어떤 속성값을 주어도 변함 없음.

### 한글 텍스트의 경우
- <td></td>태그에 아무런 속성을 주지 않은 경우 <td>넓이에 따라 자연스럽게 줄바꿈 됨.
- <td>태그에 `white-space:nowrap`이 추가된 경우는 <td>넓이를 지정하여도 줄바꿈 되지 않음.

## Refer
[여기 참조함1](http://htglss.tistory.com/31)
[여기 참조함2](http://holytv.co.kr/xe/?mid=qt01&page=5&document_srl=188)
[여기 참조함3](http://aboooks.tistory.com/189)
[여기 참조함4](https://www.w3schools.com/cssref/css3_pr_word-break.asp)
