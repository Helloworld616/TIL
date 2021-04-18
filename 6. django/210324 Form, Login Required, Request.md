## ModelForm과 Form

모델 폼은 request.POST가 첫 번째 인자로 들어오지만 그냥 폼은 request.POST를 뒤에서 받는다.

- ModelForm
  - ArticleForm
  - UserCreationForm
  - CustomUserChangeForm
- Form
  - AuthenticationForm
  - PasswordChangeForm,



## 삭제 시에 login_required를 쓰면 안되는 이유

login_required는 next parameter 주소로 redirect 해준다. 이 때 redirect가 GET 방식이므로 재접속 시에 @required_POST에서 막히게 된다.



## Django response request

> 레퍼런스
>
> - https://docs.djangoproject.com/en/3.1/ref/request-response/
> - https://docs.djangoproject.com/en/3.1/topics/auth/customizing/#substituting-a-custom-user-model