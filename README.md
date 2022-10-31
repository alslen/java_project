# 프로젝트 소개
자바로 작성한 카드 맞추기 게임입니다. 
# 개발 환경
- eclipse
- JAVA

# 프로젝트 설명
* JFrame위에 JPanel을 2개 배치했습니다.
  - panel1<br>
  ![panel1](https://user-images.githubusercontent.com/114123460/198942207-70da2603-87f6-4534-b912-302901b0b65b.PNG)
  - panel2<br>  
  ![panel2](https://user-images.githubusercontent.com/114123460/198942363-4f3f6056-71e4-4f7c-8aad-1250ed6d8696.PNG)
  
* New Game 버튼을 클릭하지 전까지는 카드 뒤집지 못하게 startCheck를 0으로 초기화
* 카드 이미지들을 JLabel 위에 배치
* New Game 버튼을 누르면 카드를 섞고 Timer(), count(남은개수)를 초기화

* 카드 클릭 시
  * 첫번째 클릭한 카드의 객체는 labelSelectedFirst에 저장 -> labelSelectedFirst에 저장 된 이미지의 이름을 int로 변환해서 firstCardNumber에 저장
  * 두번째 클릭한 카드의 객체는 labelSelectedSecond에 저장 ->  labelSelectedSecond에 저장 된 이미지의 이름을 int로 변환해서 SecondCardNumber에 저장
  * firstCardNumber == SecondCardNumber면  count의 값을 -2 해줌, labelSelectedFirst,labelSelectedSecond의 이름을 checked로 바꿈.<br>
  -> checked로 지정된 패를 누르면 실행을 못하게 하기 위해서 
  * firstCardNumber != SecondCardNumber면 카드 0.3초 보여주고 카드 다시 뒤집혀진다.

* 카드가 다 맞추면 JDialog로 결과화면을 띄운다.
* 결과화면에서 확인 버튼을 누르면 다시 게임할 수 있게 JDialog만 사라지게 만들었고, 종료버튼을 누르면 CardPuzzle(main)창까지 닫게 만들었다.

# 프로젝트 결과 화면
##### 1. New Game!! 버튼 클릭하기 전 메인 화면(카드 클릭x)
![캡처1](https://user-images.githubusercontent.com/114123460/198935561-6771d2f1-084c-4313-b3cd-cfcd915317c4.PNG)
##### 2. New Game!! 버튼 클릭한 후 화면(카드가 다 섞이면 나타나는 화면)
![캡처2](https://user-images.githubusercontent.com/114123460/198937746-2f5c47f0-ca04-4e05-a4ff-c031b66bec5e.PNG)
##### 3. 같은 카드를 찾았을 때의 화면
![캡처4](https://user-images.githubusercontent.com/114123460/198938421-66d96f79-ece5-4ff6-9be4-f48f30f16c9b.PNG)
##### 4. 카드를 다 맞췄을 때 나오는 화면
![캡처3](https://user-images.githubusercontent.com/114123460/198938708-c5319218-3474-43ca-9329-63b605802c0b.PNG)

# 이슈
1. 클래스 별로 파일을 분리하고 싶었지만 해결하지 못했음.
2. 결과 확인 창에 종료버튼을 추가하니 Congratulations메시지와 몇 초 걸렸는지 알려주는 문구가 한줄에 나오는 문제점이 생겼음. <br>
![2](https://user-images.githubusercontent.com/114123460/198992042-6c12f701-aedd-44e7-b3dd-83e1fc110e77.jpg) <br>
-> 확인버튼/종료버튼을 하나의 Panel에 추가하고 Panel(버튼들이 추가된)과 문구들을 GridLayout으로 묶어줬음.<br>
![화면 캡처 2022-10-31 200250](https://user-images.githubusercontent.com/114123460/198993915-06c32116-f9c6-4f0a-a507-deb593bb56a2.jpg)

# 추가할 기능
1. 로그인/ 회원가입/ 랭킹을 보여주는 창 구현
2. DB 테이블(멤버 테이블)을 만들어서 자바와 연동
3. 소켓을 이용해 player들끼리 경쟁하는 기능도 추가할 예정.

[출처] https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=battledocho&logNo=220034112878


