---  
layout: post  
title: "[리뷰] Do it! 안드로이드 앱 프로그래밍(개정 7판)"  
subtitle: "Do it! Android App Programming"  
categories: review  
tags: review book android app programming    
comments: true  
header-img: img/review/2020-04-03-review-book-doit-android-10-1.jpg  
---  
  
## 개요  
> 본 리뷰는 `이지스퍼블리싱` 출판사 `"Do it! 안드로이드 앱 프로그래밍(정재곤 저)"`을 읽고 얻은 지식을 정리한 글입니다.  
  
- 목차  
- [시간이 많지 않은 분들을 위하여 (요약소개)](#시간이-많지-않은-분들을-위하여-요약소개)  
- [개정 7판에서 달라진 점](#개정-7판에서-달라진-점)  
- [변화무쌍한 안드로이드의 폭풍속에서 살아남는 법](#변화무쌍한-안드로이드의-폭풍속에서-살아남는-법)  
- [백견이 불여일타! 일단 무조건 App 하나 만들고 시작한다.](#백견이-불여일타-일단-무조건-app-하나-만들고-시작한다)
- [화룡정점. 한 줄 일기장 앱 만들기.](#화룡정점-한-줄-일기장-앱-만들기)
- [그럼에도 약간 아쉬운 점은?](#그럼에도-약간-아쉬운-점은)
- [누가 읽어야 하는가?](#누가-읽어야-하는가)  
- [책의 구성 및 요약](#책의-구성-및-요약)  

  

## 시간이 많지 않은 분들을 위하여 (요약소개)
---  
본 도서를 한마디로 표현하자면 `안드로이드 앱 개발의 많은 진입 장벽을 단 한권으로 끝내주는 책`이다. 

* 개정 7판에서 달라진 점 
  - 개발환경은 `안드로이드 10` 버전 기반
  - 코틀린을 지원하기 위해 외부 라이브러리가 `androidx`로 통합 변경
  - 리사이클러뷰(RecyclerView) 등 `최신 기술이 잘 반영`되어 개발자의 스킬을 한층 업그레이드 할 수 있는 기회를 제공

* 좋았던 점
  - 컨텐츠의 지속적인 업그레이드 : `7판 2쇄` 발행(독자들의 수요가 지속되어 어마어마한 판매량을 기록했다는 의미)
  - 개발자가 개발에만 집중할 수 있게끔 마치 형상관리 해주는 느낌
  - 학습 보조 네트워크 : `유튜브 강의, 개정 PDF파일, 저자와 소통이 가능한 테크다운 카페`
  - 극단적 실전 위주 구성 : `28p에 바로 첫 번째 앱 만들기` 코너가 등장
  - 최종 프로젝트 : `한 줄 일기장 앱` 만들기
  - 대부분의 <Do it!> 시리즈가 그렇듯 `초보자도 비전공자도 따라하기 쉬운 구성`으로 되어있음
  - 학습 능률을 높이기 위한 구성 : 장박사의 조언 코너, 따라하는 과정 곳곳에 가독성을 보장하는 시각화 처리 등

* 아쉬운 점
  - 구글 Play Store에 앱 등록하기 파트의 누락
  - 앱 아키텍처 설계자 혹은 고수를 위한 챕터도 포함되었으면 하는 아쉬움
  - 보다 상세화된 목차의 필요성

보다 자세한 정보가 필요하시다면 이어지는 챕터를 계속 읽어주시기 바란다.

* [책소개 - Do it! 안드로이드 앱 프로그래밍(개정7판)](http://www.yes24.com/Product/Goods/87609520?Acode=101)
* [유튜브 강의](https://www.youtube.com/watch?v=nN4xnEcnjE8&list=PLG7te9eYUi7sjJzJR2i5m6wv-X_7K2pVE)
* [테크다운-저자 네이버 카페](https://cafe.naver.com/techtown)
* [이지스퍼블리싱 홈페이지 - 로그인 후 개정 PDF파일, 깃허브 소스 제공](http://www.easyspub.co.kr/)


## 개정 7판에서 달라진 점
---  
25년 전 즈음으로 기억한다. 책이 지금처럼 많지 않았던 시절에 어느책에선가 `좋은책을 고르는 법의 Tip`이 소개된 적이 있었는데 그때 읽었던 몇 구절이 지금까지도 좋은 책을 고르는데 도움이 되고 있다. 

그 Tip들 중 하나가 책의 "판, 쇄"를 보는것인데 현 시점 필자가 읽고있는 <Do it! 안드로이드 앱 프로그래밍>의 경우로 예를 들면 `7판 2쇄 발행`이다. 벌써 7번째 전면개정을 했다는 의미이며 나온지 얼마되지 않아 2번째의 인쇄를 거쳤다는 것인데 이는 `독자들의 수요가 지속되어 어마어마한 판매량을 기록했다는 의미이기도 하며, 오랜시간 경쟁에서 살아남아 지속적으로 개정판을 발행할 수 있는 여건을 갖춘 책`이라는 의미이다. 

이 책이 안드로이드 앱 개발 모바일 분야에서 다년 간 베스트셀러로 등극되어온 사실은 대부분의 IT분야 특히, 모바일 앱 개발 종사자들은 잘 알고 있는 사실이다. 

관련 직군의 프로그래머라면 한번쯤은 거쳤을 책이며 2010년 전후로 모바일 서비스의 수요가 급증하면서 비전공자들의 진입장벽을 낮추는데 기여한 책이라고 생각한다. 이미 시중에 판-쇄를 거듭하며 리뷰도 많이 작성된 바 책의 장점은 충분히 알려졌을 것이기에 먼저 개정판에서 달라진 내용을 소개하고자 한다.

* 개정 7판의 주요 변경사항  
  - 본 개정판의 개발환경은 `안드로이드 10` 버전 기반이다.
  - 특히, 코틀린을 지원하기 위해 `외부 라이브러리가 androidx로 통합 변경`되었다.
  - 다만 본 서적은 코틀린이 아닌 Java를 기본으로 사용한다.
  - ![개정7판](https://telegeam.github.io/assets/img/review/2020-04-03-review-book-doit-android-10-4.jpg)
* 개인적으로 느낀 주요 변경사항
  - 개인적으로 이미 예전에 읽었던 개정 4판 1쇄 버전과 비교했을때의 향상된 장점을 요약해보았다.
  - 가장 눈에띄는 장점은 역시 `최신기술이 잘 반영`되어 있다는 점이다. 예를 들면 4판까지는 리스트 등의 선택 위젯을 개발할 경우 주로 리스트뷰, 그리드뷰, 스피너 기술을 활용하여 개발하였는데, 이번 개정판에선 `리사이클러뷰(RecyclerView)`를 활용하여 이전 기술들을 교체했다. RecyclerView는 메모리를 효율적으로 사용할 수 있도록 캐시 매커니즘이 구현되어 있으며 스크롤링에 특화된 기술이다. 실제 [안드로이드 공식 개발자 가이드](https://developer.android.com/guide/topics/ui/layout/recyclerview)를 참고해보면 "앱에서 대량의 데이터 세트 또는 자주 변경되는 데이터에 기반한 요소의 스크롤 목록을 표시"하고 싶은 경우 리사이클러뷰를 사용할 것을 권장하고 있다.
  - 이처럼 본 도서는 사용자 측면에서 UI로 확인하면 큰 변화가 없는것 같은 부분도 항상 `최신기술을 활용하여 개발자의 스킬이 한층 업그레이드` 될 수 있도록 도와준다. 지속적인 개정판이 나올 수 있는 이유이며 독자로서 상당히 신뢰감이 느껴진다. 이외에도 눈에 띄는 기술의 변화가 많아 다루고 싶지만 리뷰 특성상 이 즈음에서 줄인다. 


## 변화무쌍한 안드로이드의 폭풍속에서 살아남는 법
---  
개인적으로 생각하는 본 도서 최고의 장점은 `컨텐츠의 지속적인 업그레이드`이다. 안드로이드는 모바일 특수성에 의해 시장이 자주 변동된다는 특성 때문에 버전 역시 변화가 빠르다. 더불어 구글의 정책 및 지원 등이 변화함에 따라 코틀린과 같은 새로운 개발환경이 등장하기도 하고 모바일 기기를 생산하는 삼성같은 업체의 변수도 있다. 

현재는 안드로이드 개발을 업(業)으로 삼고 있진 않지만 취미로 간간히 접할때마다 변화하는 속도를 따라가기 어렵다고 느낀다. 모바일 앱 개발이 본인도 직접 활용할 수 있고 마켓에 바로 올려 시장의 반응도 볼 수 있기 때문에 다른 프로그래밍에 비해 흥미로운 요소가 많다는 점이 장점이라면 Trade-off 측면에서 그에 못지 않은 단점도 있다고 생각하는데 그 부분이 바로 `변화의 빈도`가 아닐까 싶다. (이 포스팅을 쓰는 현재 벌써 최근 안드로이드 11 버전의 개발자 프리뷰가 등장했다.)

본 도서는 개정 7판이 등장하기까지 저자, 출판사 모두 주기적으로 안드로이드의 변화에 대응할 수 있도록 책을 업그레이드 해준다. `개발자가 개발에만 집중할 수 있게끔 마치 형상관리 해주는 느낌`이 들며, 책으로도 안드로이드의 변화를 쫓아가지 못할 경우를 대비해 `유튜브 강의, 개정 PDF파일, 저자와 소통이 가능한 테크다운 카페` 등 다양한 학습 서비스도 제공된다. 아래에 학습에 도움이 되는 URL 경로를 정리해보았다.

* [유튜브 강의](https://www.youtube.com/watch?v=nN4xnEcnjE8&list=PLG7te9eYUi7sjJzJR2i5m6wv-X_7K2pVE)
* [테크다운-저자 네이버 카페](https://cafe.naver.com/techtown)
* [이지스퍼블리싱 홈페이지 - 로그인 후 개정 PDF파일, 깃허브 소스 제공](http://www.easyspub.co.kr/)


## 백견이 불여일타! 일단 무조건 App 하나 만들고 시작한다. 
---  
분야마다 양질의 서적을 가르는 기준은 다양하겠지만 적어도 IT 분야에 있어서 만큼은 백견이 불여일타가 최고의 기준이라고 생각한다. 아무것도 모르는 채로 출발한다는 가정하에 `직접 만들어보고 눈에 보이게 해주고 사용도 해봐야 흥미도 생기고 실체도 느낄 수 있고 그래야 다시 책의 원문으로 돌아왔을때 학습의 능률을 높여줄 수 있다`고 생각하기 때문이다. 

본 도서 역시 그런 극단적 실전 위주의 구성이 마음에 들었다. 안드로이드의 개요를 대충 설명하고 개발환경을 구성하자마자 `28p에 바로 첫 번째 앱 만들기 코너가 등장`한다. 참고로 이 책의 `총 페이지수가 848p`임을 감안한다면 다른 책들로 비유할 경우 책 표지 넘기자마자 알려준 것도 없는데 App부터 만들어야 하는 느낌과 유사할 것이다. 

아니, 방법도 안 알려주고 목적지에 도착하라니? 그러면 안 좋은책 아닌가? 라고 생각하실 수도 있겠지만, 사실 처음으로 도전하는 앱은 아래 그림과 같이 버튼 3개정도 붙어있는 조촐한 앱이다. 
![첫번째앱만들기](https://telegeam.github.io/assets/img/review/2020-04-03-review-book-doit-android-10-5.jpg)

책에도 `타이밍`이라는 것이 중요하다고 생각하는데 2010년 즈음 안드로이드 시뮬레이터를 처음 켜고 두근거렸던 생각이 든다. 직접 핸드폰 다루듯 시뮬레이터 위에 앱을 터치해보면 학습 능률이 수직상승하게 된다. 초보자, 비전공자도 28p부터 필자가 느꼈던 감정을 느낄 것이기에 848p 책의 대항해를 출발하기 전 흥미로 의지를 굳게 다질 수 있지 않을까 생각한다. 

## 화룡정점. 한 줄 일기장 앱 만들기.
---  
사람마다 학습 방법은 다르겠지만 필자는 독자분들이 70페이지 분량의 첫째마당을 독파하신 후 먼저 셋째마당으로 건너뛰어 본인의 앱을 먼저 만들어보시길 권유드리고 싶다. 

특히 이미 안드로이드 개발 경험이 있는 독자이거나 뚜렷히 어떤 앱을 만들지 목표가 있는 스타트업 개발자라면 더욱 그렇다. 당장 만들고 싶은 앱이 없다면 만들고 싶은 앱을 떠올린 후 `첫째마당 -> 셋째마당 -> 둘째마당`의 순서로 읽길 권유드리고 싶은데 셋째 마당은 실전에서 필요한 대부분의 기술이 집약되어있으며 원하는 프로젝트의 숲을 먼저 경험할 수 있는 기회를 가질 수 있기 때문이다. 

그렇게 본인의 학습 위치의 좌표를 명확히 설정한 후 둘째마당의 다양한 기술을 익힌다면 기억도 오래 지속되고 특히 두번째, 세번째 앱을 만들때마다 필요한 레퍼런스를 빨리 찾을 수 있는 `일종의 메타지식`을 얻을 수 있기 때문이다. 
![최종프로젝트](https://telegeam.github.io/assets/img/review/2020-04-03-review-book-doit-android-10-2.jpg)

둘째마당의 구성은 안드로이드 앱 개발에 필요한 다양한 기술들로 이루어져 있다. 예를 들어 13장의 멀티미디어 다루기의 경우 카메라, 동영상, 오디오를 처리할 수 있는 기술에 대해 다루는데 지금 당장 만들고자 하는 앱에 동영상 재생기능이 필요없다면 자칫 집중력이 떨어질 수 있기 때문이다. 

당장의 필요에 의한 학습과 개발이 집중력을 높여주는 것은 당연하다. 앞서 설명한바와 같이 848p의 분량은 결코 쉬운 분량이 아니므로 시작도 하기 전에 지치는 것은 바람직하지 않다고 생각한다. 

## 그럼에도 약간 아쉬운 점은?
---  
충분히 많은 장점과 높은 완성도에도 불구하고 개인적으로 이번 개정7판에 약간의 아쉬운 점을 정리해보았다.
* 구글 `Play Store에 앱 등록하기` 파트의 누락
  - 구글의 정책에 민감한 플레이 스토어에 앱을 등록하는 과정은 매우 쉬운편이나 가끔 1%의 까다로움이 존재한다. 
  - 최근 페이스북 페이지에서 한 개발자가 영구 계정 정지를 당한 사례도 있었는데 원인을 알아봐도 구글 특유의 정책에 위반되었다는 답변만 돌아와 개발자의 마음을 아프게 한 사연이었다. 어쩌면 이 부분이 누락된 이유가 초보자가 호기롭게 앱을 먼저 등록하고자 시도하다가 위와 같은 안좋은 사례를 당할 수 있어서 이번 개정판에서 제외된것이 아닐까 하는 추측도 든다. 
  - 하지만 그런 위험성을 충분히 알려주고 본 챕터를 포함시키는 편이 관련 경험이 없는 초보자들에게는 큰 힘이 될 듯 싶어서 아쉬운 부분으로 남긴다. 
* 앱 `아키텍처 설계자 혹은 고수를 위한` 챕터도 포함되었으면 하는 아쉬움
  - MVPP, RxAndroid와 같은 아키텍처 부분이나 Jetpack과 같은 실전에서 활용하기 좋은 기법이나 팁도 다루어 준다면 다음 단계의 심화과정을 준비하는 분들께 많은 도움이 될 수 있을 듯 하다. 
  - 마찬가지로 이전 판에서 다뤄졌던 NFC 근거리 통신 SQLite의 상세한 활용법 같은 부분이 누락된 것도 아쉽다. 
  - 물론 이미 포화상태인 지면의 제약을 감안할 때 내용을 추가한다는 것은 어려운 일일 것이기에 이건 단점이라기 보다는 개인적인 바램이다. 때문에 이제 충분히 유명해진 본 서적도 초급편, 중급편, 고급편 등으로 레벨을 차등화하면 어떨까 싶은 바램이 있다.
* 보다 `상세화된 목차`의 필요성
  - 본 책의 지면이 상당한 관계로 보다 목차가 상세화되어 메타 지식을 구조화할 수 있으면 더욱 학습효과에 도움이 되지 않을까 싶다. 예전에 매우 상세한 목차덕에 둘째 마당에서 필요로 하는 기술을 바로바로 찾아갈 수 있었던 장점이 있었는데 이번 판은 그런 부분이 좀 더 어려워보여 약간의 아쉬움이 남는다.

그럼에도 본 도서는 장점 투성이다. 사실 열거한 아쉬움들도 일종의 자기 자신과의 싸움처럼 초반부터 7판까지 이어져 온 다른 버전의 개정판들과 비교했을때 아쉬운 부분을 설명한 정도이다. 

이것으로 책에 대한 소개를 마칠까 한다. 안드로이드 앱 개발에 관심이 있는 분이라면 누구라도 본 도서를 추천드리고 싶다. 안드로이드에 관심이 많은데 한번도 관련 책을 보지 못한 분들은 반드시 이 책으로 시작하시기 바란다. `책 한권으로 많은 초반 진입장벽을 뛰어넘을 수` 있을테니 말이다.

## 누가 읽어야 하는가?  
---  
- 안드로이드 앱 개발에 관심있는 모든 분.  
- 과거 안드로이드 앱 개발 경험이 있으나 최신 기술을 접하지 못한 분.
- 그 외 초보자 혹은 비전공자로 난이도 진입장벽에 막혀 앱 개발을 포기했던 분.
  
## 책의 구성 및 요약  
---  
이 책은 크게 세부분으로 구성되며, 각 파트에서 다루는 내용을 아래와 같이 요약해 보았다.  
  
- __1. 안드로이드 개요 (첫째마당)__    
  - 안드로이드의 개요 및 개발환경 구성
  - 첫번째 앱 만들기 및 실제 단말 연결
  
- __2. 안드로이드 완벽 가이드 (둘째마당)__   
  - 안드로이드 스튜디오와 친숙해지기, 레이아웃 익히기, 기본 위젯 사용, 화면 간 전환 등  
  - 프래그먼트, 서비스와 수신자, 선택 위젯, 애니메이션 등
  - 스레드와 핸들러, 서버와의 통신, 데이터베이스, 멀티미디어, GPS, Push 등

- __3. 실전 앱 만들기 (셋째마당)__   
  - 한 줄 일기장 앱 만들기