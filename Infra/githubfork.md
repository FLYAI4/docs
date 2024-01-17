# Github 조직 Repo 협업하기(with Github Fork)

- 조직 repo를 Fork를 통해 본인 repo에 가져 온 후 git clone으로 로컬에서 작업하기!!

<br>

## 1. Fork 하기
- 조직 repo에서 fork 버튼 클릭

<img width="937" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/a9770eca-ca48-410d-a646-07ff6418956b">

<br>

## 2. reository name 설정 후 "Create Fork" 버튼 클릭
- repo이름은 본인 계정에 생성할 repo이름이기 때문에 자유롭게 설정 가능


<img width="568" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/ccd6862e-769d-4562-b4e6-c8750639ce28">

<br>

## 3. 본인 repo를 본인의 local 환경에서 작업하기 위해 클론 작업 진행

- 해당 repo 주소 복사

<img width="719" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/e47885fe-3aea-469a-9acc-cec0c1fb963c">

- 로컬 컴퓨터 터미널 들어가서 git clone 진행

```sh
git clone {복사된 주소 입력}
```

<img width="616" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/22827a3e-fc3a-4649-ae67-7fed08132f25">

<br>

## 4. 클론된 repo 접속 후 작업을 위해 upstream, branch 설정

- branch 명은 실무에서 규칙은 있지만 현재는 작업자가 자유롭게 결정하기!!

```sh
cd ~/{경로명}

# upstream 설정
git remote add upstream {복사된 주소 입력}

git checkout -b {새로운 브런치명}
```



<img width="620" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/05807331-4be9-40ee-ab8a-be009a9f3fa3">

<br>

## 5. 작업 진행하기

- COMMIT을 한번에 하기 보다는 작업 단위별로 해주기!!

```sh
git add .
git commit -m "{커밋 메시지}"
```

<img width="510" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/83dec377-e47c-41c8-83db-954b5b40101a">

<br>

## 6. 작업이 완료되어 github에 푸시 진행

```sh
git push origin {브런치 명}
```

<img width="461" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/875230b3-408f-42dc-8ad3-c2a7dc0eb5cb">

<br>

### 6-1. Git push 인증 오류시

- Github에 Authentication OTP 설정한 계정의 경우 기존 비밀번호 입력 시 아래와 같은 오류 발생

<img width="614" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/6796bad9-325a-4c1b-97ca-04b96cf5aa89">

- Github 계정 세팅 버튼 클릭

<img width="935" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/52bc3f8e-c45e-4800-b293-be8217c6bf3b">

- Development Setting 클릭

<img width="989" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/9e5d8fe4-32b2-497e-b47d-83c3aa044241">

- Personal Access token -> token -> Generate token -> Generated new token(Classic) 클

<img width="686" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/9d0b5abc-d8bd-4254-8962-822c277e7de3">

- token 명 입력 및 모든 repo에 권한 준 후 토큰 생성

<img width="614" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/6783fc15-858b-4a73-8356-5c982b115416">

- 생성된 토큰 값 잘 저장해놓기!!!

- 다시 git push 할 때 비밀번호 입력시 해당 토큰 값 입력

<img width="545" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/18c87836-0e71-44bb-8dcd-c9e84cf3df75">

<br>


## 7. Github에 내 개인 repo로 들어가서 PR 요청

- 내가 작업한 브런치 기준 Compare & Pull Reqeust 버튼 클릭

<img width="692" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/3efe220e-f7df-4bef-b59d-08ed4c28a4ff">

- base Repository 경로 확인
- 주요 변경사항 내용 작성
- Reviewer 요청(민준을 지정해야 나한테 알림이 옴!!!)
- 위의 작업 다 끝나면 Create Pull 버튼 클릭

<img width="963" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/da8e6147-7627-4a9b-a72e-f2f5dc9be5de">

## 8. PR 요청이 완료되면 관리자가 확인 후 merge 진행

<br>

## 9. 관리자가 merge 이후 본인 개인 repo 최신으로 유지
- Update 버튼 클릭

<img width="695" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/d39992f6-25fe-4806-ba88-d2d0bea529f5">

<br>

## 10. 새로운 작업을 할 경우 local에서도 최신으로 유지 

```sh
# main 브런치 이동
git checkout main

# github 기준 최신 가져오기
git pull origin main


```


