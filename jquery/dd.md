# 화면 클릭시 원하는 타켓으로 스크롤하여 이동하기

##
```css
.box{ box-sizing:border-box; border:1px solid #F00; width:200px; height:1000px; }
#target{ width:100px; height:100px; background:blue; }
```
```html
<div class="box"></div>
<div id="target"></div>
<div class="box"></div>
```
```script
$(function(  ){
			var oriTop;
		$(window).click(function(  ){

			/*offset() 함수 : 어떤 요소의 문서 상의 상대적인 현재 위치를 알 수 있다.
			객체의 속성 중 top, `eft값을 반환해준다.*/
			var top=$('#target').offset().top; //top==1000


			/*scrollTop() 함수 : 조건에 일치하는 요소들 중 첫번째 요소의
			스크롤바의 수직 위치(y좌표)를 얻을 수 있다.*/
			oriTop=$('body').scrollTop();
			console.log(oriTop);

			$('body').animate({'scrollTop':top})
		})
	})
```
## Refer
[](http://findfun.tistory.com/249)
[](http://findfun.tistory.com/337)
