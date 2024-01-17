<img width="719" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/dc6cd214-69ae-49dc-914a-2bce4bb91d5f"># Github 조직 Repo 협업하기(with Github Fork)

- 조직 repo를 Fork를 통해 본인 repo에 가져 온 후 git clone으로 로컬에서 작업하기!!


## 1. Fork 하기
- 조직 repo에서 fork 버튼 클릭

<img width="937" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/a9770eca-ca48-410d-a646-07ff6418956b">

## 2. reository name 설정 후 "Create Fork" 버튼 클릭
- repo이름은 본인 계정에 생성할 repo이름이기 때문에 자유롭게 설정 가능


<img width="568" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/ccd6862e-769d-4562-b4e6-c8750639ce28">

## 3. 본인 repo를 본인의 local 환경에서 작업하기 위해 클론 작업 진행

- 해당 repo 주소 복사

<img width="719" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/e47885fe-3aea-469a-9acc-cec0c1fb963c">

- 로컬 컴퓨터 터미널 들어가서 git clone 진행

```sh
git clone {복사된 주소 입력}
```

<img width="616" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/22827a3e-fc3a-4649-ae67-7fed08132f25">


## 4. 클론된 repo 접속 후 작업을 위해 branch 설정

- branch 명은 실무에서 규칙은 있지만 현재는 작업자가 자유롭게 결정하기!!

```sh
cd ~/{경로명}

git checkout -b {새로운 브런치명}
```



<img width="620" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/05807331-4be9-40ee-ab8a-be009a9f3fa3">


## 5. 작업 진행하기

- COMMIT을 한번에 하기 보다는 작업 단위별로 해주기!!

```sh
git add .
git commit -m "{커밋 메시지}"
```

<img width="510" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/83dec377-e47c-41c8-83db-954b5b40101a">



## 6. 작업이 완료되어 github에 푸시 진행

```sh
git push origin {브런치 명}
```

<img width="461" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/875230b3-408f-42dc-8ad3-c2a7dc0eb5cb">


### 6-1. Git push 인증 오류시

- Github에 Authentication OTP 설정한 계정의 경우 기존 비밀번호 입력 시 아래와 같은 오류 발생

<img width="614" alt="image" src="https://github.com/robert-min/flyai-docs/assets/91866763/6796bad9-325a-4c1b-97ca-04b96cf5aa89">

- Github 계정 세팅 버튼 클릭

![Uploading image.png…]()














## 7. 




