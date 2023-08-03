## html, css, js를 이용한 계산기 프로그램 클론코딩
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/a5e1ca71-e3d4-4023-87bc-34f054921f3f)
## 함수 설명
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/f8418418-8cc7-4c92-a804-ed3dd6507cfd)   
1. runningTotal : 결과값을 저장하는 변수방
2. buffer : 사용자가 클릭한 숫자 또는 연산자를 저장하는 변수방
3. previousOperator : 이전 연산자를 저장하는 변수방

const의 내용은 screen에 html문서에서 class가 "screen"인 요소를 선택하여 저장하는 것 screen은 계산기의 화면에 해당함.   
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/606e059b-6d51-4839-b280-048896e713eb)
- - - 
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/1124bbde-7d10-43e5-a173-cdce1bea92fc)   
웹이 켜지면 이 함수부터 실행이 된다. 이 함수는 클래스명이 "calc-buttons"인 요소가 클릭 되면 buttonClick 함수를 실행하는 함수이다.   
html 문서에서 클래스명이  "calc-buttons"인 것은 말 그대로 계산기의 숫자, 연산자 버튼을 의미한다.
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/c6e3662f-44fb-4843-b8d0-1a0ec2ab6782)   
이 함수는 사용자가 누른 버튼이 숫자가 아닌 경우엔 handleSymbol함수 호출, 숫자가 맞는 경우엔 handleNumber함수를 호출하고 계산기 화면에 출력해주는 함수이다.
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/6b6b756b-e755-487c-9d92-c5cb04b148f1)   
handleSymbol함수는 연산자를 눌렀을 때 실행됨으로 switch문을 통해 각각의 연산자의 역할을 넣어주고 사칙연산자는 따로 함수를 만들어 처리한다.    
C : 화면, 결과값, 연산자 초기화    

= : 처음으로 누른 버튼이 연산자가 아니라면 flushOperation함수를 호출해 값을 계산하여 buffer에 저장하고 결과값을 초기화 함으로써 다음 계산 준비를 함.    

← : buffer의 길이가 1이라면 0으로 바꾸고 아니라면 한자리씩 지우되, 마지막 1자리에서 지우면 0으로 바꾸기   

사칙연산 : handleMath함수 호출.
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/399f0777-8df5-4132-b6e7-8b1492f62520)   
handleMath함수는 buffer = 0(사용자가 바로 연산자를 눌렀을 때)이면 무시하고 아니면 intBuffer에 buffer를 정수형으로 파싱하여 저장하고   
진행중인 값(runningTotal)를 0과 비교하여 0이면 현재 buffer값 저장을 하고 아니면 연산을 하는 flushOperation함수를 호출한다.   
그리고 연산자가 눌리면 previousOperator에 선택된 연산자를 저장하고 buffer 초기화 한다.
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/0e2a6142-cef0-4dab-8031-db232df1b492)   
연산처리를 하는 함수이다.
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/0415d6e8-eddc-4da8-8ce0-44b290971005)   
숫자가 눌렸을 때 호출되는 함수이다. screen에 선택된 숫자를 뿌려준다.
- - -
## 새로 알게 된 점
1. css의 새로운 명령어들을 알게 됨 (backdrop-filter, overflow, flex관련 여러 명령어 등등..)
2. 계산기에서 처음 계산한 값에서 그 값으로 또다시 계산하는 알고리즘을 알게 되었다.
3. js코드에서 addEventListener(이벤트 추가) 기능을 알게 되었다.
- - -
## 어려웠던 점
1. js를 이번에 처음 써봐서 코드를 이해하는 부분에서 어려웠음. (구글링을 통해 해결)
2. 계산기에서 처음 계산한 값에서 그 값으로 또다시 계산하는 알고리즘을 이해하는데 오래걸림. (메모장에 적으면서 해보니 바로 해결)
3. css에서 처음보는 명령어들이 많이 나와서 당황했음. (구글링을 통해 해결)
