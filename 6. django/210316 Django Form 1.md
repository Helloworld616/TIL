## 1. Django roles in forms

1. 렌더링을 위한 데이터 준비
2. 데이터에 대한 HTML forms 생성
3. 클라이언트로부터 받은 데이터 수신 및 처리



## 2. Django HTML input 태그 표현 2가지

1. form fields
   
   - 입력에 대한 유효성 검사 로직을 처리하며 템플릿에서 직접 사용됨
2. widgets
   - 웹페이지에서 HTML input 요소 렌더링을 처리
   - 위젯은 반드시 form fields에 할당됨!
   
   

## 3. Form과 ModelForm의 차이

- Form은 모델과 관련 없는 데이터를 받을 때, ModelForm은 저장해야 하는 데이터를 받을 때 사용한다!
- Form이 더 안 좋은 기능인 것이 아니다! 역할이 다를 뿐이다.



## 4. render와 redirect의 차이

- GET 방식은 url이 넘어간다.
- 데이터를 넘길 때에는 POST 방식을 사용한다. 데이터를 url 방식으로 넘길 경우 데이터 구조가 모두 노출되어 위험하기 때문이다. 
- render : 서버가 템플릿을 보여주는 것 (request의 method가 GET일 때)
- redirect : 주소로 다시 요청을 보내는 것 (request의 method가 POST일 때)