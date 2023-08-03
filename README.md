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
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/c6e3662f-44fb-4843-b8d0-1a0ec2ab6782)   
html 문서에서 클래스명이  "calc-buttons"인 것은 말 그대로 계산기의 숫자, 연산자 버튼을 의미한다. 이 함수는 사용자가 누른 버튼이   
숫자가 아닌 경우엔 handleSymbol함수 호출, 숫자가 맞는 경우엔 handleNumber함수를 호출하고 계산기 화면에 출력해주는 함수이다.
- - -
![image](https://github.com/hwan06/Calculator-Clone-Coding/assets/114748934/6b6b756b-e755-487c-9d92-c5cb04b148f1)   
handleSymbol함수는 연산자를 눌렀을 때 실행됨으로 switch문을 통해 각각의 연산자의 역할을 넣어주고 사칙연산자는 따로 함수를 만들어 처리한다.    
C : 화면, 결과값, 연산자 초기화    

= : 처음으로 누른 버튼이 연산자가 아니라면 최종값 buffer에 저장, flushOperation함수를 호출해 값을 계산하여 buffer에 저장하고 결과값을 초기화 함으로써 다음 계산 준비를 함.    

← : buffer의 길이가 1이라면 0으로 바꾸고 아니라면 한자리씩 지우되, 마지막 1자리에서 지우면 0으로 바꾸기   

사칙연산 : handleMath함수 호출.

