# 이쁜 게시판 만들기
> 부트스트랩이란 프론트엔트 프레임워크를 활용해 쉽게 웹사이트를 꾸며봅니다

## [부트스트랩](https://getbootstrap.com/)이란?
![bootstrap](http://www.w3.org/2000/svg)
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