# 이쁜 게시판 만들기
> 부트스트랩이란 프론트엔트 프레임워크를 활용해 쉽게 웹사이트를 꾸며봅니다

## [부트스트랩](https://getbootstrap.com/)이란?
![bootstrap](https://v4-alpha.getbootstrap.com/assets/brand/bootstrap-social-logo.pngs)
세계에서 가장 인기 있는 프론트엔드 라이브러리로 자신의 아이디어를 빠르게 구현하는데 도움을 주는 오픈소스 툴킷입니다.

* 모바일, PC, 태블릿 등 다른 크기의 디스플레이에 대응 가능한 반응형 웹
* 미리 만들어진 수많은 컴포넌트
* jQuery를 기반으로 구축된 강력한 플러그인

코드를 만져보며 게시판을 이쁘게 만들어봆니다

# [기본적인 게시판 만들기](https://github.com/haedal-with-knu/djangoBootcamp/blob/master/dashboard.md) 코드 가져오기

`기본적인 게시판 만들기` 강의에서 만든 코드를 정리해두었습니다  
가져옵니다  
```console
root@goorm:/workspace/djangoBootcamp# git clone https://github.com/kei01138/bootCamp_Week3
```

`bootCamp_Week3` 폴더 내부의 `mysite` 폴더를 `bootCamp_Week3`,`manage.py`와 같은 위치에 있도록 밖으로 꺼냅시다  
`변경 후`
```
.
|-- bootcamp_Week3
    |-- ...
|-- mysite
|-- manage.py
|-- README.md
```
마우스로 왼쪽의 폴더 트리에서 꺼내도 되고,  
리눅스 커맨드를 이용해 꺼내도 됩니다  
```console
root@goorm:/workspace/djangoBootcamp# mv bootCamp_Week3/mysite/ /workspace/djangoBootcamp/mysite
```


### `웹서버 실행` 복습  

**프로젝트를 실행할때마다 반복해서 사용하는 명령어입니다**  
파이썬 가상환경 설정 
```console
root@goorm:/workspace/djangoBootcamp/mysite# source myvenv/bin/activate
```
이제 `django` 웹서버를 실행합시다   
구름 IDE를 사용하는 경우  
상단 메뉴바의 `프로젝트 -> 실행 URL과 포트`에서   
80번 포트를 설정 후 접속합니다
```console
(myvenv) root@goorm:/workspace/djangoBootcamp/mysite# python manage.py runserver 0:80 
```

#### `Bootstrap` `CDN`
`HTML`에서 `<head>`태그엔 중요한 정보지만   
눈에 보이지 않는 정보들이 포함됩니다.

[`Bootstrap` 홈페이지](https://getbootstrap.com/)에 가면  
`CDN`을 확인 할 수 있습니다  
![img/bootstrapCDN.png](https://github.com/haedal-with-knu/djangoBootcamp/blob/master/img/bootstrapCDN.png)

`Bootstrap` `CDN`을 복사해 `<head>` 태그 안에 아래의 코드를 삽입합니다

아래와 같이 붙이면 됩니다  
`mysite/main/templates/main/index.html`
```html
<html>
    <head>
        <title>Django Tutorial</title>
        <!-- Bootstrap CDN -->
        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

        <!-- Bootstrap CSS -->
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    </head>
    <body>
        <h1>메인 페이지입니다</h1>
        <!-- 정적 이미지 불러오기 -->
        {% load static %}
        <img src="{% static 'firstImg.png' %}">
    </body>
</html>
```

