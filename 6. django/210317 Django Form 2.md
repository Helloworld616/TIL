## 1. Meta

- Meta는 models class에 대한 정보를 등록하는 곳이다.

  ```python
   class Meta:
       model = Article
       fields = '__all__'
  ```

  

## 2. Form과 ModelForm

- Form은 모델과 연관되지 않는 데이터를 수신할 때 사용
- ModelForm은 모델에서 필요한 양식의 데이터를 수신할 때 사용
- ModelForm이 Form보다 더 나은 것이 아니다! 역할이 다른 것이다.



## 3. HTTP Status code

https://developer.mozilla.org/ko/docs/Web/HTTP/Status



## 4. Django-bootstrap-v5

https://pypi.org/project/django-bootstrap-v5/