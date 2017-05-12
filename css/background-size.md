# 브라우저 화면 전체를 이미지도 덮는 방법

## 문제점
브라우저 화면 전체를 이미지로 덮으려고 ` background-size:cover` 속성을 사용했는데 작동안함.


## 해결방법
```css
	/*body 및 html의 높이를 100%로 설정하면 배경 이미지가 전체 페이지를 덮을 수 있다*/
	body,html{ height:100%; }
	/*배경 지역이 배경이미지로 완전히 덮히게 하려면 : background-size:cover*/
	.bgimg{ background-image:url(https://www.w3schools.com/w3images/forestbridge.jpg); height:100%; background-position:center;  background-size:cover; }
,,,
```html
	<html>
		<body>
			<div class="bgimg">
				<div class="topleft"></div>
			</div>
		</body>
	</html>
,,,

## 속성 값
| Value | Description |
| ---- | --- |
| auto | 기본값. 배경 이미지 원래의 너비와 높이가 그대로 표시 |
| length | 배경 이미지의 너비와 높이를 설정. 첫 번째 값은 너비, 두 번째 값은 높이. 하나의 값만 주어지면 두 번째 값은 "auto"로 설정됨. |
| percentage  | 상위 요소의 백분율로 배경 이미지의 너비와 높이를 설정. 첫 번째 값은 너비를 설정하고 두 번째 값은 높이를 설정한다. 하나의 값만 주어지면 두 번째 값은 "auto"로 설정됨. |
| cover  | 배경 영역이 배경 이미지로 완전히 덮힌다. |
| contain  | 이미지 너비와 높이가 내용 안졲에 들어갈 수 있도록 이미지를 가장 크게 조절함.|
| initial  | 기본값으로 설정. |
| inherit  | 부모 요소에서 상속. |



## Refer
[이 공부는 여기를 참조함1](http://aboooks.tistory.com/165)
[이 공부는 여기를 참조함2](https://www.w3schools.com/cssref/css3_pr_background-size.asp)