# -<!-- localhost:8080/파일이름.html -->

# 웹 퍼블리싱 중간고사 대비

##  1. 웹 프로그래밍의 개요

### 첫번째 웹 페이지

```html
<!DOCTYPE html>
<html>
	<head>
		<title> HTML의 시작 </title>
	</head>
	<body>
		<p> HTML을 시작합니다. </p>
	</body>
</html>

```

### html 문서 동작 확인

```html
<!DOCTYPE html>
<html>
	<head>
		<title> TOMCAT 웹 서비스 시작</title>
	</head>
	<body>
		<h2> 차세대 웹 프로그래밍을 시작합니다. </h2>
		<h3> 웹의 세계로 초대합니다. </h3>
	</body>
</html>

```

### jsp문서 동작 확인

```jsp
<%@page contentType="text/html; charset=utf-8" pageEncoding="utf-8"%>
<html>
<head>
	<title>TOMCAT 웹 서비스 구축</title>
</head>
<body>
	<h3>TOMCAT 웹 서비스 시작하기 </h3>
	<%
		String myname = “홍길동";
		String today = (new java.util.Date()).toLocaleString();
	%>
	<strong><%= myname %></strong> 홈페이지에 오신 것을 환영합니다.<br></br>
	오늘은 : <%= today %> 입니다.
</body>
</html>

```

## 2. HTML5 문서의 작성 규칙

l**<meta>**

-문서를 만든 이, 검색 시 키워드, 웹 페이지 정보, 리프레시 등을 작성할 때 사용

<base>

문서 내 모든 링크의 기준이 되는 URL을 지정

```html
<!doctype html>
<html>
<head>
	<title> HTML5 메타정보</title>
	<meta charset="UTF-8">
	<meta name="author" content="최병규">
	<meta name="keywords" content="HTML5, CSS3">
	<meta http-equiv="refresh" content="10; url=http://www.naver.com">
	<base href="http://www.hanyang.ac.kr">
</head>
…… 생략 …..


```

### 줄 바꾸기 + 수평선 삽입

br 태그와 hr 태그

### **하이퍼링크**

![image-20221023151626257](https://user-images.githubusercontent.com/76269640/197396047-6d398449-c9fe-4b65-b820-7d41c9f997a8.png)

### 글머리 기호 목록 태그

ul 태그

글머리 기호



li 태그

목록요소

### 순서 번호 목록 태그

ol태그

순서번호목록 생성

![image-20221023153258906](https://user-images.githubusercontent.com/76269640/197396057-ded1c7f9-c3f7-4df6-8a55-c6a67eb092b8.png)



### 테이블 태그

•table 태그

− Table의 시작과 끝을 나타냄

− 표의 테두리를 나타내려면 속성으로 **border=“1”**을 넣어주어야 함.

•tr 태그

−표의 한 행을 나타냄

•td 태그

−표에 들어가는 일반 요소를 나타냄

•th 태그

−표의 제목 요소를 나타냄

−텍스트가 굵어지고 가운데 정렬이 됨

![image-20221023205033932](https://user-images.githubusercontent.com/76269640/197396070-48fa4449-4d8c-412d-b75e-5e393754094e.png)

```html
<html>
<head>
<meta charset="EUC-KR">
<title>초간단 테이블</title>
</head>
<body>
    <table border="1">
	<th>테이블</th>
	<th>만들기</th>
	<tr><!-- 첫번째 줄 시작 -->
	    <td>첫번째 칸</td>
	    <td>두번째 칸</td>
	</tr><!-- 첫번째 줄 끝 -->
	<tr><!-- 두번째 줄 시작 -->
	    <td>첫번째 칸</td>
	    <td>두번째 칸</td>
	</tr><!-- 두번째 줄 끝 -->
    </table>
</body>
</html>
```



![image-20221023205115571](https://user-images.githubusercontent.com/76269640/197396079-843ce7e2-f66b-493a-9bb4-8be6c0be5f43.png)

![image-20221023205132955](https://user-images.githubusercontent.com/76269640/197396077-8b1b6b11-3828-4d44-933a-5a9b8608f049.png)



### 이미지 태그

![image-20221023160341234](https://user-images.githubusercontent.com/76269640/197396096-898aee04-6767-45cd-afe3-fdad651547f1.png)

l**<****img****>** **태그 속성**

-**src** : 이미지 파일이 저장된 경로 지정

-**border** : 이미지 경계선의 두께를 픽셀 단위로 지정

-**alt** : 이미지를 웹 브라우저에서 표시하지 못했을 경우 표시되는 대체 텍스트 지정

-**width/height** : 이미지의 가로, 세로 길이를 픽셀 단위로 지정(% 단위를 사용하면 웹 브라우저의 크기에 따라 이미지 크기가 조절되도록 지정할 수 있음)

-**style** : 이미지의 스타일(크기, 위치 등)을 픽셀 단위로 지정

-**title** : 이미지에 대한 설명 텍스트 

#### 이미지에 하이퍼링크 연결

![image-20221023180445990](https://user-images.githubusercontent.com/76269640/197396115-32aceee5-e945-4476-82cf-3b585aafdd82.png)

#### 이미지에 제목 추가

![image-20221023180544966](https://user-images.githubusercontent.com/76269640/197396119-36ebc13a-95dc-4a2c-ae09-67c296495cdc.png)

## **Chapter 05****입력 양식 태그와 공간 분할 태그**

### 폼 태그

```html
<form name = "입력 폼 이름" action = "웹 프로그햄 페이지" method = "전달 방식">
    <input type = "폼 모양과 기능" name = "입력 폼 변수" value = "전달 값">
</form>
```

•**name** : 폼의 이름 결정

•**action** : 사용자가 입력한 데이터를 받아 처리하기 위한 웹 프로그램(ASP, PHP, JSP… 등)의 페이지 지정

•**method** : 웹 서버와 클라이언트 간의 통신 방법 지정(GET 방식, POST 방식)

•**type** : 폼의 모양과 기능 결정

### get 방식

![image-20221023181451393](https://user-images.githubusercontent.com/76269640/197396132-839f2a27-385c-4d76-8b0a-be152358f68c.png)

#### get 방식으로 데이터 전송하기

```html
<!DOCTYPE html>
<html>
	<head>
    	<title> Get 방식</title>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    </head>
    <body>
        <h2>
            GET 방식으로 데이터 전송
        </h2>
        <form action ="getdata.jsp" method="get">
            <p>이름 : <input type = "text" name ="name" size = "15" maxlength = "12"></p>
            <p>전공 : <input type = "text" name ="major" size = "15" maxlength = "12"></p>
            <input type = "submit" value = "전송">
            <input type = "reset" value = "다시작성"> 
        </form>
    </body>
</html>
```

#### get 방식으로 데이터 요청하기

```jsp
<%@page language="java" contentType = "text/html;charset=utf-8" pageEncoding = "utf-8"%>

<html>
    <head>
        <title>get 방식 요청</title>
    </head>
    <body>
        <!-- JSP 문법 작성 -->
        <%
        		String strName = request.getParameter("name");
        		String strMajor = request.getParameter("major");
        		out.println("이름:" +strName + "<br/>");
        		out.println("학과:" +strMajor + "<hr/>");
        %>
    </body>
        
</html>
```



### post 방식

![image-20221023181540736](https://user-images.githubusercontent.com/76269640/197396137-3a1c472c-a29b-43d9-9edf-0d042abfe6f4.png)

####  POST 방식으로 데이터 전송하기

```html
<!DOCTYPE html>
<html>
	<head>
    	<title> Get 방식</title>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    </head>
    <body>
        <h2>
            GET 방식으로 데이터 전송
        </h2>
        <form action ="postdata.jsp" method="POST">
            <p>이름 : <input type = "text" name ="name" size = "15" maxlength = "12"></p>
            <p>전공 : <input type = "text" name ="major" size = "15" maxlength = "12"></p>
            <input type = "submit" value = "전송">
            <input type = "reset" value = "다시작성"> 
        </form>
    </body>
</html>
```

#### post 방식 요청

```jsp
<%@page language="java" contentType = "text/html;charset=utf-8" pageEncoding = "utf-8"%>

<html>
    <head>
        <title>POST 방식 요청</title>
    </head>
    <body>
        <!-- JSP 문법 작성 -->
        <%
        		request.setCharacterEncoding("UTF-8");
        		String strName = request.getParameter("name");
        		String strMajor = request.getParameter("major");
        		out.println("이름:" +strName + "<br/>");
        		out.println("학과:" +strMajor + "<hr/>");
        %>
    </body>
</html>
```

### 비밀번호 폼

```html
<form action="아무거나.jsp">
    <p>PW : <input type="password" name="psw" size="15" placeholder="비밀번호 입력" required></p>
</form>
```

placeholder="비밀번호 입력" -> 힌트를 의미

required -> 값이 채워지지 않으면 제출을 할 수 없음

### **텍스트 공간** **입력**

```html
<body>
    <h2>텍스트 공간 입력 양식</h2>
    <form>
        <textarea name="intro" rows="5" cols="50">
                    텍스트를 작성하는 공간입니다.</textarea>
        <p></p>
        <input type="submit" value="전송">
        <input type="reset" value="다시작성">
    </form>
</body>
```

### 라디오 입력 양식

```html
<input type = "radio" name = "gender" value="male" checked> 남성
<input type = "radio" name = "gender" value="female" > 여성
```

### 체크박스

```html
<h3> 현재 관심을 가지고 있는 학습 주제는 무었입니까?</h3>
<input type="checkbox" name="subject" value="HTML5" checked>HTML5 <br>
<input type="checkbox" name="subject" value="CSS3" > CSS3<br>
<input type="checkbox" name="subject" value="Javascript" >Javascript <br>
<input type="checkbox" name="subject" value="Jquery" >Jquery <br>
```

동시에 여러 항복을 받기 때문에 jsp 에서도 변화가 생긴다.

```jsp
<%@page language = "java" contentType = "text/html; charset=utf-8" pageEncoding = "utf-8" %>

<!DOCTYPE html>
<html lang="ko">
<head>
    <title>체크박스</title>
</head>
<body>
    <b>현재 관심을 가지고 있는 학습 주제는 </b><br/>
    -------------------------------------<br/>
    <!-- JSP문법 작성 -->
    <%
        request.setCharacterEncoding("utf-8");
        String[] StrSub = request.getParameterValues("subject");

        for(String value : StrSub){
            out.println(value + "<br/>");
        }
    %>
    -------------------------------------<br/>
    입니다~
</body>
</html>
<!-- localhost:8080/checkbox.html -->
```

### 선택 목록 양식

- html

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <title>선택 목록 양식</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
</head>
<body>
    <h3>여행가고 싶은 나라를 선택하세요.</h3>
    <form action="jsp/select.jsp" method="post">
        <select name="country" size="4" multiple>
            <option value="미국" selected>미국</option>
            <option value="일본" >일본</option>
            <option value="중국" >중국</option>
            <option value="러시아" >러시아</option>
        </select>
        <p></p>
        <input type="submit" value="제출">
        <input type="reset" value="다시작성">
    </form>

    
</body>
</html>
```

- jsp

```jsp
<%@page language = "java" contentType = "text/html; charset=utf-8" pageEncoding = "utf-8" %>

<!DOCTYPE html>
<html lang="ko">
<head>
    <title>선택 목록 양식</title>
</head>
<body>
    <h3>내가 가고 싶은 나라</h3>

    <!-- JSP문법 작성 -->
    <ul>
    <%
        request.setCharacterEncoding("utf-8");
        String[] StrCountry = request.getParameterValues("country");

        for(String value : StrCountry){
            out.println("<li>");
            out.println(value);
            out.println("</li>");
        }
    %>
    </ul>
</body>
</html>
<!-- localhost:8080/select.html -->
```

### 숫자 입력 지정 양식

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <title>숫자 양식</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
</head>
<body>
    <h3>나이를 입력하세요.</h3>
    <form action="jsp/number.jsp" method="post">
        <input type="number" name="count" min="1" max="130">
        <p></p>
        <input type="submit" value="완료">
        <input type="reset" value="초기화">
    </form>
</body>

</html>
```

```jsp
<%@page language = "java" contentType = "text/html; charset=utf-8" pageEncoding = "utf-8" %>

<!DOCTYPE html>
<html lang="ko">
<head>
    <title>숫자 양식</title>
</head>
<body>
    <h3>내가 선택한 숫자</h3>

    <!-- JSP문법 작성 -->
    <ul>
    <%
        request.setCharacterEncoding("utf-8");
        String StrNumber = request.getParameter("count");

        
        out.println(StrNumber);
    %>
    </ul>
</body>
</html>
<!-- localhost:8080/number.html -->
```

### 이메일

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <title>이메일 양식</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
</head>
<body>
    <form action="jsp/email.jsp" method="post">
        <h3>이메일을 정확하게 입력하세요.</h3> 
        이메일 : <input type="email" name="myemail">
        <p></p>
        <input type="submit" value="제출">
        <input type="reset" value="다시작성">

    </form>
</body>

</html>
```

```jsp
<%@page language = "java" contentType = "text/html; charset=utf-8" pageEncoding = "utf-8" %>

<!DOCTYPE html>
<html lang="ko">
<head>
    <title>이메일 양식</title>
</head>
<body>
    <h3>내가 입력한 이메일</h3>

    <!-- JSP문법 작성 -->
    <ul>
    <%
        request.setCharacterEncoding("utf-8");
        String StrEmail = request.getParameter("myemail");
        out.println(StrEmail);
    %>
    </ul>
</body>
</html>
<!-- localhost:8080/email.html -->
<!-- 이번 시험은 선택목록까지 -->
```

과제
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <title>회원가입</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
</head>
<body>
    <form action="quiz.jsp" method="post">
        <h3>▶ 회원가입</h3>
        <table border="1">
            <tr>
                <td>*아이디:</td>
                <td><input type = "text" name = "ID" size = "15" maxlength = "12" required></td>
            </tr>
            <tr>
                <td>*이름:</td>
                <td><input type = "text" name = "name" size = "15" maxlength = "12" required></td>
            </tr>
            <tr>
                <td>*비밀번호:</td>
                <td><input type = "password" name = "PSW" size = "15" maxlength = "12" placeholder="암호 입력" required></td>
            </tr>
            <tr>
                <td>성별</td>
                <td>
                    <input type = "radio" name = "gender" value="남성" checked> 남성
                    <input type = "radio" name = "gender" value="여성" > 여성
                </td>
            </tr>
            <tr>
                <td>나이</td>
                <td><input type="number" name="age" min="1" max="130"></td>
            </tr>
            <tr>
                <td>이메일</td>
                <td><input type="email" name="myemail"></td>
            </tr>
            <tr>
                <td>취미</td>
                <td>
                    <input type="checkbox" name="habit" value="등산" checked>등산
                    <input type="checkbox" name="habit" value="운동" > 운동
                    <input type="checkbox" name="habit" value="독서" >독서
                    <input type="checkbox" name="habit" value="영화감상" >영화감상
                </td>
            </tr>
            <tr>
                <td>자기소개</td>
                <td><textarea name="intro" rows="5" cols="50">여러분 반갑습니다</textarea></td>
            </tr>
            <tr align = "center">
                <td colspan="3" ><input type="submit" value="확인">
                <input type="reset" value="다시작성"></td>
            </tr>
        </table>

        <p></p>
    </form>
</body>

</html>
```

```jsp
<%@page language = "java" contentType = "text/html; charset=utf-8" pageEncoding = "utf-8" %>

<!DOCTYPE html>
<html lang="ko">
<head>
    <title>회원가입</title>
</head>
<body>
    <h3>▶ 회원가입 내용 ◀</h3><hr/>

    <!-- JSP문법 작성 -->
    <%
        request.setCharacterEncoding("utf-8");
        String StrID = request.getParameter("ID");
        String StrName = request.getParameter("name");
        String StrPSW = request.getParameter("PSW");
        String StrGender = request.getParameter("gender");
        String StrAge = request.getParameter("age");
        String StrMyemail = request.getParameter("myemail");
        String[] StrHabit = request.getParameterValues("habit");
        String StrIntro = request.getParameter("intro");
        out.println("아이디 :" +StrID + "</br>");
        out.println("이름 :" +StrName + "</br>");
        out.println("패스워드 :" +StrPSW + "</br>");
        out.println("성별 :" +StrGender + "</br>");
        out.println("나이 :" +StrAge + "세" + "</br>");
        out.println("이메일 :" +StrMyemail + "</br>");
        out.println("취미 :");

        for(String value : StrHabit){
            out.println(value + " / ");
        }
        out.println("</br>" + "자기소개 :" +StrIntro);
    %>
</body>
</html>
<!-- localhost:8080/select.html -->
```
