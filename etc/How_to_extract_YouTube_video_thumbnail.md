# 유튜브 영상 썸네일 추출하는 방법


## 1. 아이디값 가지고 오기.
동영상이 있는 페이지에서 **공유** 클릭  후 `https://youtu.be/아이디값`에서 아이디 값 복사하기.


## 2. 아이디값을 입력하고 브라우저에 붙여넣으면 끝

1. 기본 (일반) : 120x90
	* http://i.ytimg.com/vi/아이디값/default.jpg"
	```html
		<img src="http://i.ytimg.com/vi/아이디값/default.jpg" alt=""/>
	```

2. 기본 (중간) : 320x180
* http://i.ytimg.com/vi/아이디값/mqdefault.jpg"
```html
<img src="http://i.ytimg.com/vi/아이디값/mqdefault.jpg" alt=""/>
```

3. 기본 (큰화면) : 480x360
* http://i.ytimg.com/vi/아이디값/hqdefault.jpg"
```html
<img src="http://i.ytimg.com/vi/아이디값/hqdefault.jpg" alt=""/>
```

4. 기본 : 640x480
* http://i.ytimg.com/vi/아이디값/sddefault.jpg"
```html
<img src="http://i.ytimg.com/vi/아이디값/sddefault.jpg" alt=""/>
```

5. 기본 : 1920x1080
* http://i.ytimg.com/vi/아이디값/maxresdefault.jpg"
```html
<img src="http://i.ytimg.com/vi/아이디값/maxresdefault.jpg" alt=""/>

```

## 활용 방법

1. 이미지 저장 후 포토샵에서 열기.
2. ctrl + n 사용하여 원하는 썸네일 크기에 맞춰 새문서 열기.
3. 이미지를 복사하여 새문서에 붙여넣기.
4. ctrl + t
5. shift 누른 채로 마우스 움직이며 새문서 사이즈에 이미지 크기 맞추면 끝.


## Refer
[이 공부는 여기를 참조함](https://gs.saro.me/#!m=elec&jn=382)