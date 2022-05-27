# YACC-Lex
YACC와 Lex
LEX와 같이 AT&T Bell 연구소에서 Mark Lesk가 UNIX 시스템의 유틸리티로 개발한 소프트웨어.
LEX가 정규표현식(Regular Expression)을 확인한다면,YACC은 문법(Grammar)를 확인한다
Input:Grammar rules & action
Yacc(or bison)
Output : C코드로 된 Parser 생성
LEX가 정규표현식(Regular Expression)을 확인한다면,YACC은 문법(Grammar)를 확인한다.
Yacc의 구조는 Lex와 같은 3개의 절로 구성(정의절 / 규칙절 / 서브루틴)_int 변수를 카운팅하는 프로그램
정의절: “y.tab.h” : 프로그래머가 만든 Yacc의 토큰 번호 & 기타 변수의 정보를 가지고 있다./ D는 숫자[0-9] / L은 변수 첫 글자 [a-zA-Z]
intcount=0으로 초기화 해준다 / lex에서 받은 토큰들을 정의 및 start 설정
규칙절: int, 변수가 가능한 문자, 숫자 ‘;’ 를 각각 반환하고 yacc.y파일에서 받아준다 / int a; / int a,b=0,c,d=1,g;
서브루틴절: yywrap: EOF를만나면 호출. non zero - 끝. zero - 다음 파일을 더 받음
Yacc Program Lex Program 은 에서 특정부분을 분석하며 읽는 내용을
넘겨받아서 특정 이벤트를 발생시킬 수 있다 이 기능을 이용하여 읽어들인 부분이 어떤 기능을 하는지를 분석하고 각 기능들에 대한 카운트를하여 출력하는 프로그램을 구현하도록 한다 문법을 바탕으로 . ANSI C 구현한다.
