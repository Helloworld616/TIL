## 1. GET 방식의 문제점

- 만약 엄청나게 내용이 긴 데이터나, 이미지가 업로드 된다면 이것을 url로 담을 수 있을까?
- 또한 게시글 작성이 아닌 로그인이라면 개인 정보도 다 노출하게 된다.
- 그래서 HTTP method POST는 HTTP body에 담아 전송한다.



## 2. REST API

- ```GET/articles/```
  - 게시글 목록 좀 줘
- ```POST/articles/```
  - 게시글 추가해줘 (수정, 삭제)



## 3. POST로 변경 후 변화하는 것

1. request.POST.get()
2. csrf token도 함께 보내주어야 함
3. 더 이상 url에 내가 넘기는 데이터가 노출되지 않음
4. POST는 HTML을 요청하는 것이 아니기 때문에 HTML 문서를 받아볼 수 있는 곳으로 다시 redirect해야 한다.