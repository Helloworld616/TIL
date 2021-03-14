### 1. CSS position

- static : 디폴트 값 (기준 위치). 보통 왼쪽 상단.
- relative : static 위치를 기준으로 이동 (상대위치)
  - top, bottom, left, right : 해당 위치에 여백 생성
  - 이동 시 과거의 자기 위치를 고정시킴!
- absolute : static이 아닌 부모/조상 요소를 기준으로 독자적으로 움직이는 경로 (절대위치)
  - 이동 시 과거의 자기 위치를 다 버림! (집 나간 자식)
  - 그 결과 다른 요소들이 이동을 해서 레이아웃에 영향을 미치게 됨
- fixed : 부모요소와 관계없이 무조건 브라우저를 기준으로 움직임.
  - 스크롤 시에도 항상 같은 곳에 위치함!



### 2. emmet cheat seat

- https://docs.emmet.io/cheat-sheet/
  
  - syntax 부분 한 번 따라치면서 연습해보기!
  



### 3. BEM (Block Element Modifier)

**전제조건 :** id를 사용하지 않는다!!! class의 이름은 길어져도 상관 없다.

```html
<div class="card"> 
  <div class="card-head">
    <div class="card-head--disabled"></div>
  </div>
  <div class="card-body">
    <div class="card-body__title"></div>
    <div class="card-body__content"></div>
  </div>
</div>
```

{block}-{block}__{element}

{block}-{block}--{modifier}