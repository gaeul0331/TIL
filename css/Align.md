# Align



## 1.  가로로 가운데 정렬

1. block element 가로로 가운데 정렬
	* **margin:auto**사용.
    * width property를 설정하지 않거나 100%로 설정한 경우 margin:auto가 작동안함.
	```html
        <style>
                .img{ display: block; margin-left:auto; margin-right: auto;  }
        </style>
    	<img class="img" src="/kge/imgs/file_icon/xls.gif" alt="">
    ```
	
2.  이미지를 가로로 가운데 정렬
	* block element로 만든 다음, margin-left:auto 와 margin-right:auto 적용.
	```html
    	<style>
                .img{ display: block; margin-left:auto; margin-right: auto;  }
        </style>
    	<img class="img" src="/kge/imgs/file_icon/xls.gif" alt="">
    ```

3. element 내부에 텍스트를 가로로 가운데 정렬
	* text-align: center; 사용.
	```html
    	<style>
                div{ border:1px solid red; box-sizing:border-box; text-align: center; }
        </style>
    	<div>center</div>
    ```

4. 가로와 세로 모두 가운데로 정렬
	* 부모의 position property의 값이 relative일 때, 자식 element는 언제나 가로와 세로 모두 가운데로 정렬.
	```html
         <style>
                .parent{ position: relative; width: 100%; height: 500px;  border:1px solid red; box-sizing:border-box; }
                .parent > .center{ width: 100px; height: 100px; border:1px solid red; box-sizing:border-box; position:absolute; top:0; bottom:0; left:0; right:0; margin:auto;}
         </style>
         <div class="parent">
             <div class="center">center</div>
         </div>
    ```
       
5. 브라우저 화면을 변경해도 언제나 가로와 세로 모두 가운데로 정렬
	* 부모의 position property의 값이 relative일 때, 자식 element는 언제나 가로와 세로 모두 가운데로 정렬.
	```html
         <style>
                .parent > .center{ width: 100px; height: 100px; border:1px solid red; box-sizing:border-box; position:fixed; top:0; bottom:0; left:0; right:0; margin:auto;}
         </style>
         <div>center</div>
    ```       

6. 가로로 가운데 정렬
	*  div에 display property 값을 inline으로 바꿔도 브라우저에서 block element로 변경해버림(신기하네 뭐지?).
	```html
         <style>
                div{ width: 100px; height: 100px; border:1px solid red; box-sizing:border-box; position:absolute; left:0; right:0; margin-left:auto; margin-right:auto; }
         </style>
         <div>center</div>
    ```

7. 세로로 가운데 정렬
	*  div에 display property 값을 inline으로 바꿔도 브라우저에서 block element로 변경해버림(신기하네 뭐지?).
	```html
         <style>
                div{ width: 100px; height: 100px; border:1px solid red; box-sizing:border-box; position:absolute; top:0; bottom:0; margin-top:auto; margin-bottom:auto; }
         </style>
         <div>center</div>
    ```                     
       




## Refer
[이 공부는 여기를 참조함](https://www.w3schools.com/css/css_align.asp)
