# 김두영
leokim1022@snu.ac.kr  |  [github](https://github.com/mori-inj)

## 이력 및 수상 내역
* 2014.3 ~ 현재: 서울대학교 컴퓨터공학부(SNUCSE) 
  * 2015.1 ~ 2016.3: SNUCSE 알고리즘 및 문제풀이 동아리 SNUPS 회장 
  * 2015년도 서울대학교 교내 프로그래밍 경시대회 운영 및 진행
  * [2015년도 전국대학생프로그래밍 경시대회 본선 7등 (팀명: EeveE)](http://icpckorea.org/2015-daejeon/regional)  
  * SNUCSE 정보보안 동아리 가디언 회원
  * SNUCSE 자유 개발 동아리 UPnL 회원 
    
* 2011.3 ~ 2014.2: 용인한국외국어대학교부설고등학교(외대부고) 
  * 2013.7: ICICS 학회지 암호 관련 [소논문](http://www.lnit.org/uploadfile/2013/1210/20131210031015753.pdf)  
  * 2012년도 전국정보올림피아드 지역대회 은상 


## 재미있게 들은 수업
* Computer Science
  * Algorithm & Data Structure   
      Array, LinkedList, Stack, Queue, Sorting, Tree, HashTable, Heap(prioriy queue), Balanced Search Tree, Graph  
      Advanced Sorting, Order Statistics, DP, DisjointSet(union-find), Greedy, String Matching, MST, ShortestPath, NP
  * Programming Principle, Automata
* Hardware
  * Logic Design
  * Hardware System Design
* System
  * Computer Architecture
  * System Programming  
      asm (low-level) programming, shell, proxy server, memory allocator, library interpostioning
  * Operating System  
      implemented new systemcall, read/write lock, scheduler queue, and gps based file system
* Graphics
* Artificial Intelligence

## Skill Set
* Windows Native
  * C/C++ (with winapi)
  * C# (with WPF)
* Problem Solving
  * C, C++ (with STL)
  * [boj.kr(최근)](https://www.acmicpc.net/user/mori_inj), [boj.kr(이전)](https://www.acmicpc.net/user/leokim1022)
* Machine Learning
  * C++
  * TensorFlow(python)
* Game
  * Unity (with C#)
* Web
  * backend: Flask(python)
  * frontend: html, css, js(including jquery)
* etc
  * graphics: openGL, C++
  * hardware description language: verilog (on FPGA)
  * Arduino, x86/x86_64 asm, Java(not frequently used)
* tools
  * vim
  * Visual Studio


## 지금까지 만든 것 (Project)
### 사자런
* 횡스크린 런게임
* Unity2D, C# 사용
* 이미지  
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/e72cf714b874bcfcd2561073f02cd531abdd8439/main.png)   
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/e72cf714b874bcfcd2561073f02cd531abdd8439/SajaRun_ingame.png)  
* 원버튼 방식   
  누르면 달리고 떼면 달린 시간에 비례해서 점프. 
  점프 중에 다시 누르면 땅으로 곧장 착지.


### [von](https://github.com/mori-inj/von) 
* 신경망 시각화([참고](http://playground.tensorflow.org/))와 유사하지만 사용자가 좀 더 interactive하게 데이터를 추가하고 신경망 모델을 바꿀 수 있게끔
* winapi, C++ 사용(C#과 WPF 조합으로 짜면 더 예쁘고 빠르게 짤 수 있었지만 런타임 속도가 중요한 프로젝트라 C++사용)
* 이미지
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/e484cb2dc90b927c8d2f2bb61795dc971d7d4cdd/von.png)  
* 신경망 구조가 꼭 층 형태가 아니더라도 backprop이 가능하게 짬
* 다양한 패턴의 2차원 데이터를 직접 입력으로 넣어볼 수 있고 실시간으로 학습함
* 은닉층의 결정경계가 어떻게 되는지, 은닉층을 독립된 입력으로 볼때 출력층과의 관계가 어떻게 되는지 등을 확인 가능
* 지금까지 혼자 작업한 프로젝트들 중 가장 코드 분량이 많음(6천줄 가량 작성 / 2천줄 가량 삭제)


### [captcha_svm](https://github.com/mori-inj/captcha_svm)
* Support Vector Machine을 사용해 [이 사이트](http://sugang.snu.ac.kr/)에서 쓰이는 숫자 캡챠 이미지를 인식
* C++ 사용 (winapi는 png 이미지 input 처리를 위해 사용)
* SVM의 특성상 학습 과정에서 훈련 데이터를 기억하고 있어야 하기 때문에, 메모리 한계로 0~9까지 숫자별로 2천개 정도의 이미지(총 2만개)로 학습
* 캡챠 데이터 자체의 왜곡 정도가 MNIST에 비해 훨씬 약하고 정자체에 가까우며, 데이터간 편차가 적기 때문에 별다른 커널 트릭 없이 선형 SVM만으로 99.7%의 정확도 달성
* 가우시안 커널 구현

von과 captha_svm 같은 머신러닝 프로젝트들은 알고리즘을 공부한 후 다른 코드를 참고하지 않고 구현하는 연습을 했음


### [3D](https://github.com/mori-inj/3D) graphics
* winapi(gdi)의 함수들 중 화면에 무언가를 그리는 데에는 화면상의 픽셀을 매개변수로 받는 MoveToEx, LineTo 두 함수만 사용하고 그 외의 모든 openGL의 rendering pipeline을 따라해 보는 게 목표
* winapi, C++ 사용
* 이미지  
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/sphere.png)
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/function.png)
* 레이캐스터까지 구현한 상태이며, cpu만 사용 && gdi의 성능상 속도에 한계가 있음


### [4D](https://github.com/mori-inj/4D) graphics
* 4차원 상의 정다포체를 3차원에 투영한 것을 3D 프로젝트를 이용해 다시 화면상에 출력
* winapi, C++ 사용
* 이미지  
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/8cell.jpg)
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/16cell.jpg)
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/24cell.jpg)
* 4차원 상에서 해당 도형의 회전이 3차원에 어떻게 투영되어 보이는지 관찰 가능
* 현재는 좌표와 선분만 옮겨졌는데 [이 영상](https://www.youtube.com/watch?v=0t4aKJuKP0Q)처럼 4차원 도형과 3차원 공간의 교공간과 rendering을 추가하는 것이 목표


### [OS](https://github.com/mori-inj/LUDOS) bootloader
* 운영체제 수업을 듣고 아쉬운 점들이 있어서 추가로 [책](http://www.hanbit.co.kr/store/books/look.php?p_code=B9833754652)을 구해 예제들 구현
* C, asm 사용
* 이미지  
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/os_color.jpg)
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/os_window.jpg)
* 운영체제 수업을 들었으나 운영체제의 특징과 기능들을 부분 부분 배웠을 뿐이라 장난감 수준이더라도 바닥부터 전체까지 운영체제를 직접 만들어보고 싶어짐
* 부트로더 관련 부분은 학과 수업에서 전혀 다루지 않았기에 더 관심이 생겼고, 평소에도 시스템콜 호출 이후부터 모니터의 특정 픽셀이 켜지고 꺼지기까지 무슨 일이 일어나는지 매우 궁금했기에 화면 출력과 관련된 부분에 초점
* 해당 이미지는 다른 프로그램의 도움 없이 bios 인터럽트만으로 원하는 이미지를 화면상에 그려낸 모습


### Office Document Structure Parsing and Analysis
* 창의적통합설계 수업 과제로 각 팀 별로 회사들이 제안한 프로젝트를 수행. [소프트캠프](http://www.softcamp.co.kr/)사의 제안으로 한 학기 동안 xlsx, docx, pptx, xls, doc, ppt, pdf의 7가지 유형의 문서 파일의 구조를 분석하고 구조이상이나 CVE취약점을 이용한 악성코드가 삽입되어 있을 경우 이를 제거하고 문서 재조합을 시도하는 프로그램을 만듦
* C#, Open Xml SDK 사용


### [NAVER movie crawler](https://github.com/mori-inj/naver_movie_crawler)
* 영화 제목 목록이 주어졌을때 그 영화의 주연 배우를 네이버 무비 페이지를 통해 크롤링함
* C, Python 사용
* 크롤링 하는 부분은 C로 작성


### [미대 과제전 협업 및 전시](https://github.com/mori-inj/misulsense)
* 관객에게 스위치가 주어지고, 스위치를 누른후 관객 스스로 느끼기에 1초가 지났다고 생각하는 시점에 스위치를 뗀다. 떼는 순간 TV화면의 디지털 시계의 1초는 관객의 1초만큼의 속도로 흐른다.
* Arduino, winapi 사용
* 이미지  
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/your_time.jpeg)
  ![](https://raw.githubusercontent.com/mori-inj/mori-inj.github.com/master/nametag.jpeg)
* 아두이노와 연결된 스위치가 chatterless switch가 아니므로 특정 시간간격보다 짧은 변화는 무시하는 C코드를 아두이노 위에 돌린다.
* PC(winapi)는 스레드 두 개를 돌린다.  
  하나는 COM port를 통해 시리얼 통신으로 아두이노가 스위치가 눌려있던 시간을 보내기를 blocking 방식으로 기다리고
  다른 하나는 화면에 출력되는 시계를 현재 설정된 시간 간격마다 갱신한다.
* 아두이노와 컴퓨터가 통신하는 코드는 다른 사람의 코드를 참고했다.


## 프로젝트 보다 작은 규모로, 새로 배운걸 바로 적용해보기 위한 컨셉 검증용 Toy Project
### 로그인 정보 전달
* 학교 학생인지 아닌지 인증을 위해 아이디 비밀번호 폼을 제공한다. 학교 포털 로그인에 사용되는 학번과 비밀번호를 입력하면 이를 받아서 학교 포털로 request 날리고 response에 따라 인증 성공, 실패 여부를 판단한다. (일종의 proxy)
* Flask 사용
* CORS 원칙 때문에 js만으로 해결하려 했으나 그러지 못했다.
* http request header는 크롬 개발자 도구에서 복붙한 뒤에 Wireshark로 실제 패킷과 비교했다.

### C++ 메일 전송 및 PostgreSQL DB 연동
* C++로 작성한 채팅프로그램의 기능을 확장해 웹서비스와 비슷한 일을 할 수 있을까 하는 생각해서 출발
* C++, [Zoho Mail](https://www.zoho.com/mail/), PostgreSQL 사용
* 채팅프로그램에 이메일을 통한 인증과 회원가입 기능을 넣고 싶어서 Zoho라는 메일 서버 역할을 할 서비스와 회원 정보를 저장할 DB 마련
* C++ 코드 상에서 Smtp 프로토콜을 통해 메일을 발송/수신하고, DB를 열고 추가/삭제/갱신 등이 가능하다는 것을 확인함


### [지뢰찾기 solver](https://github.com/mori-inj/minesweeper)
* Windows XP 버전 지뢰찾기 게임을 자동으로 푸는 프로그램
* winapi 사용
* 찍어야 하는 상황이나 추론해야하는 상황을 해결할 수는 없고, 현재 주어진 숫자와 판세에 대해 즉각적으로 풀 수 있는 경우에만 푼다.
* 지뢰찾기 프로그램의 픽셀 영역을 비트맵 형식으로 읽어와 숫자의 색상에 따라 숫자를 구분한다.

  

