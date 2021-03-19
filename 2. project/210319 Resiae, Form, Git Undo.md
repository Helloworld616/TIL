## 1. Resize

https://pypi.org/project/django-imagekit/



## 2. Form

- Request and response objects

  https://docs.djangoproject.com/en/3.1/ref/request-response/

- 500대 에러 제거하기 : get_object_or_404() 사용

  https://docs.djangoproject.com/en/3.1/intro/tutorial03/



## 3. Git Undo

- Staging Area에 있는 파일을 Unstaging 상태로 바꾸기

  ```bash
  git rm --cached a.txt
  ```

- commit 메시지 수정하기

  ```bash
  git commit --ammend
  i 눌러서 끼워넣기 모드로 바꾸기 (esc 누르면 취소)
  commit 메시지 이름 수정 후 esc 누르기
  :wq 입력 후 엔터를 치면 저장됨
  ```

  - vim 사용법 : https://www.openvim.com/

- 새로운 파일을 기존 commit에 추가하기

  ```bash
  git add d.txt
  git commit --ammend
  :wq 입력 후 엔터를 치면 저장됨
  ```

- 과거의 commit으로 돌아가기

  ```bash
  git log --oneline (commit의 아이디 값 확인)
  git reset --hard commit의 아이디 값
  
  git log --oneline (commit의 아이디 값 확인)
  git reset --soft commit의 아이디 값
  
  git log --oneline (commit의 아이디 값 확인)
  git reset --mixed commit의 아이디 값 (mixed가 디폴트 값이라 생략해도 무방함)
  ```

  - hard는 과거로 완전히 돌아감 (히스토리 삭제, add 기록 없어짐)
  - soft는 과거로 돌아가지만 기록을 삭제하기는 않음 (히스토리 남겨둠, add 기록 남아있음)

  