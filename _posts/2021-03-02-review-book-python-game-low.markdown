---  
layout: post  
title: "[리뷰] 파이썬으로 배우는 게임 개발 입문편"  
subtitle: "퀴즈, 주사위, 제비 뽑기, 미로, 진단 애플리케이션, 블록 낙하 퍼즐, RPG 등을 만들며 배운다!"  
categories: review  
tags: review book Python Pygame Tkinter Game GUI CUI 블록낙하 객체지향 OOP RPG 남코 닌텐도 코나미
comments: true  
header-img: img/review/review-book-python-game-low-1.png
---  
  
> `제이펍` 출판사의 `"파이썬으로 배우는 게임 개발 입문편(히로세 츠요시 저/김연수 역)"`를 읽고 작성한 리뷰입니다.  

![표지](https://telegeam.github.io/assets/img/review/review-book-python-game-low-1.png)  

---

본 도서는 파이썬을 활용하여 게임을 개발하는 방법을 다룬다. 내용이 방대하기에 굵직한 장점을 먼저 소개하고 타임라인 순으로 읽으며 느꼈던 점들을 소개하는 방식으로 리뷰하려 한다.

* __살을 버리고 뼈를 취하는 구성__  
  게임 서적을 읽다 지치는 가장 큰 이유는 방대한 소스코드의 무덤 속에서 길을 잃고 숲을 헤매는 구성 때문일 것이다. 이 책은 핵심 완급조절을 분명히 하는 장점이 있다.

  언리얼이나 유니티 라이브러리는 구현에 상당한 편리함을 가져다 주지만 가려진 밑바닥을 보기 힘들기에 배우고 나면 뭔가 붕 뜬 느낌이 있다. 잘 모르고 가져다 쓰기만 한 라이브러리에 때문에 자신감도 떨어지고 흥미도 떨어진다. 

  Tkinter 모듈을 활용하여 `밑바닥`도 건드려 보고, PyGame 모듈로 군더더기를 날려버리고 `핵심`에 집중해 보는 등의 완급조절이 일품이었다. 자세한 내용은 아래 세부 설명에서 소개하겠다.

* __저자의 경력과 실력__  
  저자는 `남코, 닌텐도, 코나미에서 25년 간 게임을 개발, 기획`한 실력자이다. 교육기관에서 강의도 담당하고 있어 전달력도 상당하다. 

* __게임을 만들고 싶게 하는 구성__  
  30 ~ 40 대 아재들은 `일본이 주도했던 PC 게임의 추억`을 잊지 못할 것이다. PC, 프로그래밍, 게임에 관심이 많았던 아재들이라면 한 번쯤 스스로 게임을 만들어 보겠다는 야망(?)도 있었을 것이다. 이 책은 밑바닥까지 게임을 구현해보기에 자신감을 키워주며 스스로 게임을 만들고 싶다는 욕구를 한 껏 불러 일으킨다.

* __디테일한 구성과 가독성__  
  내용 자체로도 훌륭한 책인데 독자들의 가독성을 높혀주는 구성상의 `완성도가 일품`이라는 장점도 무시할 수 없다. 약간 덕후스럽지만 애니메이션의 두 여자 캐릭터가 학습을 도와주며, 부록편엔 게임 동아리도 등장하여 `게임하듯 배울 수 있다`. 

  각 장마다 등장하는 컬럼에 대한 재미도 쏠쏠하다. 게임 업계에 대한 정보도 가득하고, 저자가 현업에서 부딪혔던 유용한 Tip들도 종종 소개되고 있다.
  ![컬럼_59p](https://telegeam.github.io/assets/img/review/review-book-python-game-low-2.png)  


책이 어떻게 구성되어있는지 보다 세부적으로 설명하기 위해 실습 예제를 따라해보며 시간의 흐름대로 느꼈던 점들을 아래와 같이 정리해 보았다. 책을 크게 3개의 파트로 나누어 설명해 보겠다. 

--- 

* __게임 개발 개요와 파이썬의 기본(1 ~ 4장)__  
  + 먼저 게임 업계는 어떻게 수익을 얻는지, 크리에이터에는 어떤 직군이 있는지, 게임의 종류와 어떻게 하면 게임 프로그래머로서의 커리어를 쌓을 수 있는지 설명한다. 게임 개발 능력을 키우기 위한 좋은 자극제가 되며 저자의 경험을 녹였기에 이해하기 쉬웠다.

  + 파이썬, 통합 개발 환경(IDLE)을 설치하고 가장 중요한 변수, 리스트, 반복문, 조건문, 함수, import에 대해 간단히 실습해본다. 고작 이 정도 학습하고 뒤에 게임들을 개발할 수 있을까 의구심이 들었는데 오히려 난잡하지 않게 게임 개발에 필요한 사항만 잘 추렸다는 생각을 했다. 게임 개발에 장점이 있다면 시각적 피드백일텐데 Tkinter, PyGame 모듈로 눈으로 보면서 구현하기에 기본에만 충실하면 나머지는 경험과 시간의 몫이 될 수도 있겠다는 생각이 들었다.

--- 

* __CUI / GUI / Tkinter(5 ~ 9장)__  
  + 먼저 CUI(문자열 기반 인터페이스) 게임을 만들어 본다. 복잡한 그래픽 요소를 일단 제쳐두고 게임 기획의 본질을 먼저 익히면서 Python에 친숙해지게 만들어준다. 주사위를 던져 나오는 랜덤한 숫자로 컴퓨터와 대결하여 누가 먼저 결승점에 도착하는지 내기하는 예제도 있는데 게임을 만들 때 필요한 기본 감각을 가장 잘 설명하는 예제라 할 수 있다. 부수적인 것보다는 `본질에 대한 감`을 익히는데 중요한 과정이라 생각한다.

  + 이어 Tkinter를 활용한 GUI(그래픽 기반 인터페이스) 개발에 돌입한다. Python에서 GUI 기반 프로그래밍에 가장 흔히 사용하는 Tkinter 모듈을 주로 사용한다. PyGame은 게임에 특화된 라이브러리인지라 처음부터 PyGame을 활용하면 라이브러리를 가져다 쓰기만 할 뿐 밑바닥을 구현하기 어렵기에 Tkinter를 활용하여 기본기를 다지는 구성이 기본에 충실하는데 좋은 구성이라는 생각했다.

  + `Tkinter의 기본 활용법`을 익힌다. 제비뽑기 프로그램을 만들어보며 라벨, 버튼, 캔버스, 텍스트, 멀티 텍스트 필드, 체크박스, 메시지 박스 등을 그리는 방법을 배운다. Visual Studio에서는 주로  버튼을 끌어와 윈도우에 배치하는데 이와 달리 Java 진영과 유사하게 SDK 방식의 직접 코딩으로 컴포넌트를 배치하는 차이점이 있다. 물론 결과는 동일하다. 모든 실습을 마치면 아래와 같은 진단 게임을 완성할 수 있다.
  ![진단게임_136p](https://telegeam.github.io/assets/img/review/review-book-python-game-low-3.png)  

  + 여기까지의 실습으로는 사실 GUI를 활용한 일반 프로그래밍이지 게임 프로그래밍이라고 하긴 어렵다. 8장에서 `게임다운 게임`을 처음으로 만들게 되는데 기술적으로 아래와 같은 기법을 실습한다.
    - after() 함수를 이용한 실시간 처리 구현
    - bind() 함수로 이벤트 처리
    - 2차원 리스트를 활용한 미로 배경 정의
  실습을 마치면 아래와 같은 미로 게임을 완성할 수 있다.
  ![미로게임_168p](https://telegeam.github.io/assets/img/review/review-book-python-game-low-4.png)  

--- 

* __PyGame / RPG 만들기 / OOP / 부록__  
  + 밑바닥 구현은 학습에는 도움되지만 노가다가 심하기에 보다 본격적인 게임 구현의 요소에 집중하고자 PyGame을 활용하기 시작한다. 

  + 마우스 이벤트 처리, 위치 데이터와 같은 상태 정보 관리, 낙하 알고리즘 구현, 점수 산출을 위한 평가 알고리즘을 구현해보며 블록 낙하 게임을 완성한다.

  + 우습게 보일지 몰라도 처음으로 게임다운 게임이 등장했다. 실제로 즐겨보면 꽤 재밌기까지 하다. 대학 때 동아리에서 슈팅 게임을 만들어 본 적이 있는데 그때 머리 싸매고 간신히 구현했던 요소들이 하나씩 다 등장하고 있다. 핵심 알고리즘에서 평가에 이르기 까지 게임 구현에 가장 중요한 요소들을 구현하고 있어 이 예제가 가장 뼈대 예제라는 생각을 했다. 요즘엔 AI에 푹빠져 강화학습을 학습 중인데 상태, 에이전트, 환경 등의 정보로 활용할만한 기능이 모두 구현되어 있기에 더욱 기본이 탄탄한 예제라는 생각을 할 수 있었다.
  ![블록낙하_213p](https://telegeam.github.io/assets/img/review/review-book-python-game-low-5.png)  

  + Tkinter에서 PyGame 기반의 구현에 익숙해지도록 PyGame을 살펴본다. Tkinter 실습때와 마찬가지로 이미지도 그려보고 키, 마우스 이벤트 처리도 실습해본다. 더불어 Tkinter에서 취약했던 사운드 출력 같은 멀티미디어 요소를 처리하는 기능도 다룬다.

  + 드디어 이 책의 하이라이트이자 게임의 꽃이라 할 수 있는 RPG를 구현한다. 개인적으로 기본적인 게임은 학창시절에 구현해 본적이 있었기에 그 단계를 뛰어넘는 첫 도전이었으며 가장 흥미로운 장이었다. 블록 낙하게임 기본 기능에서 `추가된 RPG 고유의 기능`은 아래와 같다.
    - 미로를 던전으로 바꾸기
    - 배경 스크롤 : 움직이며 배경이 변하기 시작한다.
    - 이동신/전투신 제작 및 상호 전환
    - 턴방식 프로그래밍
  ![RPG](https://telegeam.github.io/assets/img/review/review-book-python-game-low-6.png)      
  11 ~ 12장은 그간 배운 지식을 바탕으로 최대한 스스로 구현해보려고 노력하면 더 좋을 것이다. 그 후 본문의 소스코드와 비교하는 과정을 거친다면 더욱 빠르고 확실한 이해가 가능해진다. 개인적으로 이 방식을 통해 스스로 복잡하게 생각했던 기능들을 게임 모듈에서 일종의 편법(?)으로 얼마나 간단히 처리하는지 아이디어를 얻을 수 있어 놀랐고, 더불어 Python으로 알고리즘을 구현하는데 친숙해지는 소득을 얻을 수 있었다. 

  + 마무리로 OOP의 개념을 다룬다. GameCharacter라는 클래스를 상속받은 검사, 닌자 등의 예제를 예로 들며 객체지향의 개념을 다루고 있다. 부록에서는 3가지 업그레이드 예제가 더 등장한다. 복습용으로 좋은 예제들이다.

---

RPG 게임까지 구현하고 나면 상당한 `자신감`이 생긴다. 구현하는 과정에서 스스로의 `아이디어`가 떠오르기도 하고 이를 녹여보는 과정에서 자연스럽게 구현 능력이 향상된다. 아들과 재미있게 게임해보고 싶어 읽은 책인데 소기의 목적을 달성하고 있어 즐겁다.

자신감이 충만해져서일까? 보다 풍부한 예제가 소개되었으면 하는 아쉬움이 있었는데 다행히도 이 책은 시리즈로 구성되어 있다. 이 책은 입문편으로 보다 심화 과정인 실전편의 책이 한 권 더 있어 안도감이 들었다. 리뷰를 쓰는 시점에 실전편의 책을 익히고 있는 중이기에 조만간 실전편 리뷰도 올릴 생각이다.

게임 업계의 꿈을 가지고 있는 이라면 반드시 읽어야 할 필독서이다. 이 책을 통해 게임 전반의 `핵심에 해당하는 뼈대 감각`을 익히고 업계에 발을 딛는 것과 숲을 보지 못하는 안목으로 이정표 없이 구현에만 급급한 것은 분명 하늘과 땅 차이다.

더불어 게임을 취미로 익히고 싶거나 Python으로 알고리즘 구현에 익숙해지고 싶은 사람에게도 강력히 추천하고 싶다. `스스로의 창의성을 구현`하는 방법을 배운다는 것은 배움 이상으로 인생에 쏠쏠한 행복을 가져다 준다.

---

* [책소개 - 파이썬으로 배우는 게임 개발 입문편](http://www.yes24.com/Product/Goods/93802364)
