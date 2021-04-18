## 역참조

타겟 모델에서 소스 모델을 참조하는 것이 역참조!

- 소스 모델
- 타겟 모델



## Symmetric

- Symmetric의 기본값은 True

   ex) 친구가 신청 한 번에 둘 다 친구로 맺어지면 Symmetric

- 팔로우는 Symmetric하지 않음



### Many To Many

- many to many 관계에서 on_delete가 없는 이유는 종속 관계가 아니기 때문이다!

- many to many의 특징 : 모델에 영향을 끼치지 않으면서 중계 테이블을 만든다.



## 안일한 최적화의 함정

- exists는 캐싱을 하지 않아 메모리를 절약할 수는 있지만, 같은 쿼리에 대한 평가를 또 수행해야 할 수도 있다.