## 1. throw 과정

1. 클라이언트가 장고 서버에 요청을 보냄 (throw 페이지를 받기 위해서)
2. '/articles/throw/' -> urls.py
3. articles 앱의 throw 뷰 함수 호출
4. throw 뷰 함수가 throw.html을 리턴
5. 이제서야 클라이언트가 throw 페이지를 받게 됨.



## 2. catch 과정

1. 데이터를 입력해서 submit
2. 클라이언트가 장고 서버로 '/articles/catch/url'로 요청을 보냄.
3. project의 urls가 먼저 받는데 '/articles/' 주소와 매칭
4. articles의 urls로 연결해서 catchpath 함수와 매칭
5. catch 뷰 함수 호출
6. throw로부터 받은 데이터를 처리 후 catch.html 문서를 만들어서 응답 보냄.
7. catch 뷰 함수가 만든 응답을 클라이언트가 받음.