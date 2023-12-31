---  
layout: post  
title: "[리뷰] 파이썬 자동화 교과서"  
subtitle: "업무 생산성을 3배 높이는 엑셀, 워드, 크롤링, 메일 자동화 기술"  
categories: review  
tags: review book 파이썬 자동화 엑셀 스크레이핑 크롤링 SNS 트위터 메일 연동 스케줄러 대화상자 웹서버 데스크톱앱 마우스 키보드   
comments: true  
header-img: img/review/review-book-python-automation-1.png
---  
  
> `제이펍` 출판사의 `"파이썬 자동화 교과서(구지라 히코즈쿠에 저/문지현 역)"`를 읽고 작성한 리뷰입니다.  

![표지](https://telegeam.github.io/assets/img/review/review-book-python-automation-1.png)  

---

> 엑셀 및 워드 작성, 크롤링, 메일 및 SNS 연동, 웹서버 구성, 정규표현식, 데스크톱 앱, 키보드 및 마우스 조작까지 Python을 활용한 사무 자동화 프로그래밍 방법이 모두 담겨있는 것이 특징이다. 

이 책은 `엑셀 및 워드 작성, 크롤링, 메일 및 SNS 연동, 웹서버 구성, 정규표현식, 데스크톱 앱, 키보드 및 마우스 조작`까지 Python을 활용한 사무 자동화 프로그래밍 방법을 모두 담고 있는 것이 가장 큰 특징이다. 

본문에 소개된 엑셀 및 워드 작성을 예로 들면 프로그래머라면 모를까 일반 사무직종 종사자라면 주어진 양식에 개인화된 정보 즉, 이름, 주소, 전화번호 등을 매번 바꿔가며 인쇄했던 경험이 분명 있을 것이다.

이 번거롭고 귀찮음은 물론 집중력이 떨어지면 실수하기 좋은 작업을 Python 코드 수십 줄이면 손쉽게 해결할 수 있다. 위 그림에 보이는 엑셀 목록의 개인화된 정보를 아래 지정된 템플릿에 하나씩 수정 반영하여 종합 산출물을 뽑아낼 수 있는 것이다. 
![자동화](https://telegeam.github.io/assets/img/review/review-book-python-automation-2.png)  
![코드](https://telegeam.github.io/assets/img/review/review-book-python-automation-3.png)  

그동안 Python을 활용한 자동화 프로그래밍 스킬을 담은 책은 여러 권 읽었지만 이 모든 내용을 모두 담고 있는 책을 찾기는 어려웠다. 각각의 주제 중 하나를 선택해 심도있게 다루거나 이 책에 담긴 일부 기술만 다루는 책들이 대부분이었다. 

유사한 서적 나름 각각의 장단점이 있지만 유사 서적 대비 본 도서의 차별화된 점이 있다면 단 한권의 책에 자동화에 관한 `거의 모든 주제`를 담았다는 점이 가장 큰 장점일 것이다. 

다음 장점으로는 일본 서적 특유의 스타일답게 하나하나의 실습 예제마다 `문제가 될 만한 소지를 최소화`했다는 점이다. 

예를 들어 OS별로 디렉토리 구분자가 다르다. 윈도우 운영체제의 경우 \\ 문자를 사용하는 반면, 리눅스 계열에서는 \/ 문자를 사용한다. 초보자의 경우 이런 부분에서 디렉토리를 인식하지 못해 오류가 나면 당황하기 쉬운데 os.path.join()과 같은 함수를 사용하여 어떤 OS를 사용하더라도 문제되지 않도록 실습을 구성하는 등 꼼꼼히 신경쓴 부분이 엿보였다.

다른 웹사이트 정보를 스크레이핑 하는 예제 또한 그렇다. 단순한 URL만으로는 가져오기 어려운 정보들이 있는데 Request 헤더를 구성하여 가져오는 방법이 소개되어 있어 꼼꼼하다는 인상을 느꼈다. 레퍼러, 쿠키, 세션 등의 정보는 HTTP 통신을 통해 주고 받을 수 있기 때문이다. 

또 다른 장점으로는 `자동화를 넘어선 유관 스킬`이 상당 부분 소개되었다는 점이다. 간단한 웹 서버를 구성하는 방법이 그런 예이다. 웹서버가 있고 없고는 자동화에 있어 큰 영향을 미친다. 일방적으로 가져오기보다는 스스로의 데이터를 주고 받기가 가능한 환경으로 구성할 수 있기 때문이다. 

그 외에도 간단한 데스크톱 앱을 만드는 방법이 소개된 점이나 정규표현식을 소개하여 문자열 검색, 추출 등의 작업의 숙련도를 업그레이드 할 기회를 준 점, 한 발자국 더 나아가 마우스나 키보드를 컨트롤하는 방법도 소개되어 있어 유익했다.
![마우스](https://telegeam.github.io/assets/img/review/review-book-python-automation-4.png)  

전체적으로 `가독성` 측면도 뛰어나다. 저자가 전달하는 내용이나 기술을 역자가 확실하게 이해한 후 번역한 흔적이 돋보였고 덕분에 한국 저자의 서적을 읽는 것처럼 편했다. 일본어로 된 실습예제는 한글 예제로 전환한 것도 인상적인 부분이다. 

`난이도`는 프로그래머 기준으로는 매우 쉬운 편이다. 사무직의 경우 찬찬히 따라하면 충분히 소화할 수 있을 듯 하다. 그래도 기본적인 Python 문법을 익히거나 적어도 타 언어 프로그래밍 기초 경험이 있다면 수월할 것이고 그렇지 않다면 약간은 어려울 수도 있다. 

부록에 기초적인 문법을 언급하고는 있지만 기본 프로그래밍 수준은 떼고 보는 것이 가장 효율적으로 책을 이해하고 활용할 수 있을거라 본다.

저자가 서문에 `사용할 사람이 직접 프로그램을 만드는 것이 이상적`이라고 소개한 내용이 읽는 내내 머릿속에 맴돌았다. 

확실히 맞는 말이다. 프로그래밍이 점차 기본 소양이 되어가는 시대에 사무직 초보 프로그래머라 할지라도 이런 쉽고 효율성을 높혀주는 책을 통해 스스로 원하는 프로그램을 만들어가다보면 업무를 쉽고 편하며 빠르게 마무리지을 수 있을 듯 하다. 

---

* [책소개 - 파이썬 자동화 교과서](http://www.yes24.com/Product/Goods/110509098)
