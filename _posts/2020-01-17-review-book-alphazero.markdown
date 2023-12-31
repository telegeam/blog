---  
layout: post  
title: "[리뷰] 알파제로를 분석하며 배우는 인공지능"  
subtitle: "Alpha Zero Artificial Intelligence"  
categories: review  
tags: review book alpha zero deep learning dqn mcts thinker tic tac toe  
comments: true  
header-img: img/review/2020-01-17-review-book-alphazero-1.jpg  
---  
  
## 개요  
> 본 리뷰는 `제이펍` 출판사 `"알파제로를 분석하며 배우는 인공지능(후루카와 히데카즈 저)"`을 읽고 얻은 지식을 정리한 글입니다.  
  
- 목차  
- [2020년 처음으로 읽은 책](#2020년-처음으로-읽은-책)
- [알파고, 알파고제로, 알파제로](#알파고-알파고제로-알파제로)  
- [딥러닝, 강화학습, 탐색의 핵심개요](#딥러닝-강화학습-탐색의-핵심개요)  
- [깨알같은 디테일로 독자의 진입장벽을 낮춘다.](#깨알같은-디테일로-독자의-진입장벽을-낮춘다)  
- [딥러닝](#딥러닝)
- [강화학습](#강화학습) 
- [탐색](#탐색) 
- [대망의 알파제로 구현!](#대망의-알파제로-구현)
- [누가 읽어야 하는가?](#누가-읽어야-하는가)  
- [책의 구성 및 요약](#책의-구성-및-요약)  
- [요약하며...](#요약하며)  
  

## 2020년 처음으로 읽은 책
---  
새해 처음으로 올리는 리뷰를 본 도서로 시작할 수 있어 상쾌하다. 지금까지 읽었던 딥러닝 계열의 도서 중 `가장 재미있고, 가장 포괄적인 내용을 다루고 있으며, 그럼에도 가장 쉬워, 가장 극찬하고 싶은 책`이다.  
  
단 `370 페이지`의 짧은 분량으로 알파고의 발전사, 파이썬 문법, 구글 Colab 및 TPU, 딥러닝, CNN, ResNet, 정책경사법, Sarsa, Q, DQN, 미니맥스법, 알파베타법, 몬테카를로 트리 탐색, 알파제로 구현, thinker를 활용한 UI 개발, 틱택토, 커넥트4, 오셀로, 간이장기...를 어떻게 다 가르쳐 줄 수 있는건지 또, 어떻게 이렇게 쉽고 재미있게 알려줄 수 있는건지 두 번에 걸쳐 정독한 지금도 믿기지 않는다.  
  
딥러닝을 몰라도, 심지어는 python을 몰라도, 조금 더 오버하자면 프로그램의 기초 개념 정도만 알아도 본 도서를 이해하는데 그리 어렵지 않을 것이다. 

가시적으로 실행 가능한 코드가 제공되고, 딥러닝의 발전 방향에 맞춰 모델 간 장단점을 비교해 나가며 핵심 차이점만 깔끔하게 전달하는 전개 방식, 그리고 심지어 구글 Colab의 자세한 사용법과 파이썬 문법까지 알려준다. 각 단원마다 재미있는 게임을 예로 들어 상상력을 전개하기 쉽게 도와주고 상상력이 원동력이 되어 이해를 돕도록 구성한 점도 특징이다.
  
왜 이렇게 극찬하는지 궁금하신 분들은 잠깐 시간내어 본 리뷰를 읽어주시기 바란다. 성격 급한 분들은 당장 책을 구매하셔서 보시는게 시간 절약 측면에서 나을 수도 있겠다. 구체적인 리뷰를 시작하기에 앞서 아래 로드맵을 참고하기 바란다. 본 도서는 로드맵이 목차보다도 깔끔하며 본 리뷰 또한 동일한 순서로 진행할 예정이다.  
![로드맵](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-2.jpg )  


## 알파고, 알파고제로, 알파제로  
---  
* `알파고`는 구글 딥마인드에서 개발한 인공지능 바둑 프로그램으로 이세돌 9단에게 4승 1패의 승리를 거두며 전세계에 AI, 데이터 사이언스의 열풍을 일으켰다.  
  
* `알파고 제로`는 알파고를 상대로 100대 0으로 압승을 거두었으며, 기보없이 셀프 플레이만으로 학습하였다.  
  
* `알파제로`는 알파고 제로보다 승률은 뛰어나고 학습 속도는 향상된 장점을 가진 최신 버전이다.  
  
본 포스팅을 읽고 계신 분이라면 일반적인 특징 보다는 기술적인 차이점에 관심이 많으실 것이다. 알파고는 지도학습과 강화학습을 혼용한데 반해 알파제로는 강화학습만 사용했다는 점이 큰 특징이고, 딥러닝 네트워크 구조에 있어 알파고는 CNN을, 알파제로는 ResNet을 사용했다는 차이점이 있다. 기타 자세한 차이점은 본 도서에서 발췌한 아래 그림을 참고하시기 바란다.  
![알파고 제로와의 차이점](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-20.jpg )  
  
  
## 딥러닝, 강화학습, 탐색의 핵심개요  
---  
1장에서는 흥미진진한 스토리로 알파제로를 간단히 설명한 후 `퍼셉트론, 딥러닝, 지도학습(분류, 회귀), 비지도학습, CNN, RNN 등 딥러닝`과 관련된 핵심 개념을 다룬다. 딥러닝을 이미 알고 있는 독자에게 핵심 지식을 깔끔하게 정리할 기회를 주고, 전혀 모르는 분도 중요한 개념을 짚고 넘어가게 해준다. 아래 그림은 AND 함수를 구현한 퍼셉트론 및 딥러닝 학습 모델에 대한 도식도이다.  
![퍼셉트론](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-3.jpg )  
![학습모델](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-4.jpg )  
  
이어서 `에이전트, 환경, 행동, 상태, 보상, 정책, 수익, 가치 등 강화학습`의 핵심 개념을 다룬다. 아래 그림은 강화학습의 용어 및 학습사이클을 설명한 부분이다.  
![강화학습 용어](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-5.jpg )  
![강화학습 사이클](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-6.jpg )  
  
이어 탐색의 핵심 개념을 다룬다. 완전 게임 트리와 부분 게임 트리를 다룸으로써 `알파베타법`이 가지는 한계와 이를 대체하기 위한 수단인 `몬테카를로 트리 탐색`의 개념을 미리 소개한다.  
![게임트리](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-7.jpg )  
  
## 깨알같은 디테일로 독자의 진입장벽을 낮춘다.  
---  
딥러닝과 알파제로의 핵심 주제에는 벗어나지만 이 책에 숨은 또 다른 공신을 찾자면 알파제로를 구현하기 위한 `파이썬 문법, 구글 Colab의 사용법, 로컬 환경 및 코랩 환경의 패키지 버전 소개 등 개발 환경 구축을 위한 정확하고 디테일한 설명` 등을 들 수 있겠다.  
  
* 예를들면 아래와 같이 책의 예제를 구현할 때 사용한 패키지 버전까지 상세하게 명시한다. 따라하기만 해도 알파제로를 만들 수 있도록 저자의 친절한 배려가 돋보인다.  
![패키지 버전](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-8.jpg )  
  
* 심지어 파이썬을 파이썬 답게 사용할 수 있는 문법을 총망라함으써 파이썬에 생소한 독자들도 쉽게 파이썬 문법에 적응하게 해준다. 두꺼운 파이썬 책을 읽다가 망각하는 것 보다 처음에 본 도서로 파이썬을 익혀도 되겠다는 생각이 들 정도였다. 
![파이썬 문법](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-9.jpg )  
  
* 더불어 돈 한푼 없어도, 뛰어난 장비 없어도 개발할 수 있도록 구글 Colab에 관하여 필수 지식을 모두 전수해준다. `90분 룰 회피하기, 12시간 룰 회피하기` 같은 Tip도 전수해주며 GPU가 아닌 TPU를 활용한 개발 방법까지도 자세하게 안내해 준다. 모든 책들이 흔히 말하지 않는 고수들만 알 법한 깨알같은 팁을 아낌없이 공유한다.  
  
이러니 도저히 개발을 못할 수가 없다. 독자들이 무엇때문에 알파제로를 개발하지 못할지 그 경우의 수를 수도 없이 고민한 장인의 냄새가 난다. 덕분에 독자들의 진입장벽이 현저히 낮아져 단언컨데 열정만 있는 독자라면 책을 덮고 난 뒤에는 프로그램을 거의 몰라도 알파제로를 만들고 상당 부분 이해하며 뿌듯해 할 것이다.  
  
  
## 딥러닝  
---  
딥러닝을 조금이라도 학습해 본 분들은 누구나 MNIST 예제 정도는 한번쯤 돌려보셨을 것이다. 방심하지 말고 다시 돌려보자. 그저 그런줄 알았던 `MNIST` 일반적인 분류 모델이 `CNN`과 어떻게 다른지 명확히 느낄 수 있는 기회다. 더불어 `ResNet`과는 어떤 차이가 있는지 비교가능하다. 아래 그림과 같은 이해를 돕는 구조도와 함께 말이다.  
![딥러닝 모델](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-10.jpg )  
![CNN 모델](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-11.jpg )  
![CNN 모델2](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-12.jpg )  
![ResNet 모델](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-13.jpg )  
  
실습 코드 구현을 통해 이미지 인식 분야의 발전 과정을 명확히 이해할 수 있다. 발전 과정에서 등장한 모델을 서로 비교하며 구현하는 과정에서 기억이 오래 남도록 유지해주는 효과를 얻을 수 있다. 

각 장별로 사용한 색상도 달라 현재 내가 어느 파트를 읽고 있는지 도와주기도 한다. 이런 저자와 편집자가 구성한 `기억 지속 장치` 덕분에 후반부의 알파제로를 구현할 때 본 장에서 배운 ResNet 지식이 대부분 되살아남을 느꼈다.  
  
   
## 강화학습
---  
다중 슬롯머신 문제를 통해 어떤 팔을 당겨야 가장 많은 돈을 벌 수 있을지 일종의 게임이론과 같은 흥미로운 주제로 강화학습에 접근한다. 탐색과 이용이라는 트레이드 오프 관계를 이해하고 균형을 맞추기 위한 아래 그림과 같은 `UCB1`에 관해 설명한다. 

수학없이 코딩만 등장하는 허접한 책이 아니다. 놀라운 것은 수식이 제법 나오는데도 거의 이해되는 신기한 책이라는 점이다.  
![UCB1](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-14.jpg )  
  
강화학습은 처음 접하면 생소한 개념에 좌절하기 쉬운데 각 절마다 개념을 알기 쉽게 예제를 통해 이해를 돕는다. 정책 경사법 또한 미로찾기 같은 재미있는 게임을 통해 핵심 개념을 설명한다.  
  
Sarsa와 Q의 개념 또한 앞서 미로찾기에 대한 설명을 활용하여 이해를 돕고 행동 및 상태 가치 함수를 `벨만 방정식`으로 정리한다.  
![벨만방정식](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-15.jpg )  
  
탄탄히 정리된 기초 개념을 통해 DQN을 정리한다. 카트-폴 게임을 가시적인 예제로 사용하여 앞서 나왔던 개념들의 장단점을 총정리하게 되며 이 과정에서 알파제로에서 사용할 정책망과 가치망이 어떤 식으로 구현되는지 감을 잡을 수 있다.  
  
  
## 탐색  
---  
일반적인 음성, 이미지, NLP 분야와 달리 게임분야 AI의 색다른 점이 있다면 바로 탐색이 아닐까 한다. `유한 확정 완전 정보` 게임이라면 더욱 탐색 기법을 사용하지 않을 수 없는데 알파제로 구현에 있어서도 역시 탐색이 핵심 기법 중 하나이다.  
  
먼저 `미니맥스법`을 통해 게임트리의 개념을 이해한 후 `알파베타법`의 가지치기 방법을 통해 계산의 속도를 높이는 방법을 배운다. 아래 그림과 같이 세부적인 예시를 들어 어떻게 탐색을 하지 않고 가지를 쳐 속도를 높일 수 있는지 이해를 돕는다.  
![알파베타법](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-16.jpg )  
  
이어 완전 게임 트리가 경우의 수가 많아질 수록 활용하기 어려운 이유를 설명하고 대체 수단인 `몬테카를로 트리 탐색`의 개념을 설명한다. 1 ~ N 회차의 시뮬레이션을 반복하며 트리 노드에 큰 변화가 있을 때 마다 아래 그림과 같이 알기 쉽게 설명해준다.  
![몬테카를로 15회차](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-17.jpg )  
  
  
## 대망의 알파제로 구현!  
---  
앞서 배운 딥러닝, 강화학습, 탐색 등 핵심 기술을 집대성하여 `알파제로`를 만든다. 알파제로에서 사용할 강화학습 사이클 및 딥러닝 네트워크의 구성 그리고 최종 완성된 틱택토 게임은 아래와 같다.  
![강화학습 사이클](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-18.jpg )  
![듀얼네트워크](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-19.jpg )  
![최종본](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-22.jpg )  
  
이 장에서는 딥러닝, 강화학습, 탐색을 어떻게 결합할 수 있는지 `소프트웨어 공학의 진수`가 담겨있는 장이기도 하다. 더불어 8장에서는 알파제로를 구현하며 만들었던 `모델을 재활용하고, 모델의 저장과 로드를 통해 커넥트4, 오셀로, 간이장기`를 개발한다. 이 과정에서 스프트웨어 공학은 물론 실무에서 이미 개발한 모델을 어떻게 변형된 모델에 적용할 수 있는지 실무 감각을 높일 수 있다.  
![간이장기](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-23.jpg )  
  
이 뿐만이 아니다. 알파제로에서는 몬테카를로 트리 탐색 시 앞서 설명한 UCB1을 활용하지 않고 아래 그림과 같은 공식의 `아크 평갓값`을 사용한다. 이처럼 필요한 분야에 적합한 수학적 모델링을 도출하고 직관적으로 이해하여 데이터와 비교 대응할 수 있는 데이터 사이언티스트의 역량을 엿볼 수도 있다.  
![간이장기](https://telegeam.github.io/assets/img/review/2020-01-17-review-book-alphazero-21.jpg )  

* [도서 미리보기](https://jpub.tistory.com/993)  
* [GitHub 소스코드](http://github.com/Jpub/AlphaZero)

## 누가 읽어야 하는가?  
---  
- ResNet, 몬테카를로 탐색 트리, DQN에 부딪혀 딥러닝 학습에 좌절을 겪은 분  
  
- 가시적인 제품 구현을 통해 딥러닝의 핵심 개념을 명확하게 이해하고 싶은 분  
  
- 알파제로를 구현하고 싶거나 알파고 관련 논문 이해에 어려움을 겪는 분 

- 기타 딥러닝에 관심이 있는 모든 분  
  
  
## 책의 구성 및 요약  
---  
이 책은 크게 세부분으로 구성되며, 각 파트에서 다루는 내용을 아래와 같이 요약해 보았다.  
  
- __1. 머신러닝의 개요, 파이썬, 구글 Colab__  
  + 알파고, 딥러닝, 강화학습, 탐색의 개요  
  + 구글 Colab의 사용법  
  + Python 문법 학습 등  
  
- __2. 딥러닝, 강화학습, 탐색의 핵심 개념__  
  + 딥러닝 : 분류, 회귀, CNN, ResNet  
  + 강화학습 : 정책경사법, Sarsa, Q, DQN
  + 탐색 : 미니맥스법, 알파베타법, 몬테카를로 탐색 트리 등  
  
- __3. 알파제로의 구현__  
  + Part2의 핵심 개념을 종합한 알파제로의 구현  
  + 알파제로의 모델을 재사용하여 커넥트4, 오셀로, 간이장기 등의 구현
  + Thinker를 활용한 UI 구현(사람과의 대전)  
  
  
## 요약하며...  
---  
2020년 새해. 처음으로 읽어도 될만한 가치가 있는 귀한 책을 만났다. 리뷰를 작성할 때는 책의 장점을 진솔하게 전달하기 위해 노력하는 편이지만 특히 이번 책의 리뷰를 소홀히 작성하는 것은 예의가 아니라는 생각이 들만큼 훌륭한 내용과 짜임새있는 품격이 느껴져 두 번에 걸쳐 정독했다.

책의 내용을 한바탕 정리하고 싶은 마음이 가득했으나 그러기엔 리뷰 수준의 분량을 넘어설 듯 하여 가급적 책의 장점만 피력하고자 노력했다. 앞서 설명한 바와 같이 `지금까지 읽었던 딥러닝 계열의 도서 중 가장 재미있고, 가장 넓은 영역을 다루고 있으며, 그럼에도 가장 쉬워, 가장 극찬하고 싶은 책`이다. 

단 `370페이지의 짧은 지면으로 알파고의 발전사, 파이썬 문법, 구글 Colab 및 TPU, 딥러닝, CNN, ResNet, 정책경사법, Sarsa, Q, DQN, 미니맥스법, 알파베타법, 몬테카를로 트리 탐색, 알파제로 구현, thinker를 활용한 UI 개발, 틱택토, 커넥트4, 오셀로, 간이장기 구현방법` 등을 모두 알려준다.   
  
딥러닝을 전혀 몰라도, 심지어는 파이썬을 몰라도, 조금 더 오버하자면 프로그램의 기초 개념 정도만 알아도 본 도서를 이해하는데 그리 어렵지 않을 것이다. `가시적으로 실행 가능한 코드가 제공되고, 딥러닝의 진화 방향에 맞춰 모델 간 장단점을 비교해 나가며, 심지어는 구글 Colab의 자세한 사용법과 파이썬 문법까지` 알려준다.  각 단원마다 재미있는 게임을 통해 개념을 전달하고자 한 시도도 눈에 띄는 특징이다.

지난 2019년 한해동안 GAN, Reinforcement Learning으로 대표되는 AI기술들과 연구 결과는 끊임없이 쏟아졌고 축적되는 관련 지식의 Volume은 점차 가속화되고 있다. BERT와 같은 기술 하나에 집중하기도 어려운데 정신을 차리고 주위를 둘러보면 MuseNet이니 GPT-2이니 주옥같은 기술들이 이미 등장하여 상용화 되어간다.  
  
본 도서를 통해 딥러닝의 빠른 발전 속에도 길을 잃지 않도록 알파제로까지의 핵심 개념을 명확히 이해하여 허리를 튼튼히 하고, 알파제로의 구현을 통해 이해에 이해를 덧칠한다면 2020년에 다가올 폭풍우도 그리 두렵지 않을 것이다. 책의 내용은 말할 것도 없고 기억을 오랫동안 지속시키기 위한 편집과 구성도 일품이라는 생각이 든다. 

아쉬운 점은 사실 없다. 굳이 애써 찾자면 텐서플로 2.0을 사용했으면 더 좋았을 뻔 했다는 점, 알파제로의 모델로 바둑을 구현했으면 좋겠다는 점이 있겠으나, 그러기엔 이 책을 늦게 만나게 되거나 실습을 포기해야 하는 트레이드 오프를 감당해야 하므로 현재로도 대 만족이다.

AI, 딥러닝에 관심이 있는 분이라면 초보자, 고수 가리지 않고 반드시 읽어보시길 바란다. 분명 무엇이든 얻게 될 것이다.

  
> \<제이펍 출판사\>  
>  
> 보통 서적에 담긴 내용의 기술적 깊이가 뛰어나면 가독성과 재미는 떨어지게 마련인데, 제이펍의 책들은 그 트레이드 오프가 성립하지 않아 개인적으로 매우 신기하다고 생각했습니다. 진정성 듬뿍담긴 깊이있는 내공을 즐겁게 흡수하고 싶다면 꼭 제이펍의 도서목록을 살펴보시기 바랍니다. 숨은 진주를 얻게 되실 겁니다.   
  
[제이펍 바로가기](https://jpub.tistory.com/)