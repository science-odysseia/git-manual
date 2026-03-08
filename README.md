#### 안내문
md기초 페이지

[MD-guide](MD-guide.md)

# Git Settings
Git 처음 배우는 사람을 위해....(사실 본인도 잘 몰라요... 안까먹으려고 작성한 문서)

여기선 Ubuntu를 사용합니다. PowerShell(PS)를 사용하는 방법은 아래 링크를 클릭하세요.

[Git-Guide-PS](git-guide-ps.md)

## 1. Github 회원가입 / 로그인
1. https://github.com 접속 (이걸 보고 있다면 이미 접속했겠지만......)
2. 계정이 없다면 'Sign up'으로 회원가입, 있다면 Sign in'으로 로그인

|![github_main](githubimgs/github_main.png)|![github_signup](githubimgs/github_signup.png)|
|---|---|

3. Username과 Email은 기억하세요. 나중에 쓰입니다.


## 2. Git 설치
1. 설치 시작

``` bash
sudo apt update
sudo apt install git -y
```

아래 명령어를 쳐서 버전이 나오면 설치성공.

``` bash
git --version
```
2. 사용자 정보 설정

아래 명령어를 입력합니다. "" 안에 있는 내용은 본인이 원하는대로 쓰시면 됩니다.

자유롭게 입력하셔도 무방합니다만 되도록이면 본인의 github 계정에 맞게 쓰시는 걸 권장드립니다.

``` bash
git config --global user.name "당신의 닉네임"
git config --global user.email "당신의 이메일(xxxx@xxxxx.com 형식)"
```

아래 명령어로 확인

``` bash
git config user.name
git config user.email
```

## 3. Repository(레포지토리) 생성
Repository(레포지토리)란?

그냥 간단히 Git 저장소에 올릴 대표 저장 폴더 정도로 생각하면 됩니다.

github.com에서 직접 추가해도 되지만

터미널을 이용해서 추가해 볼 예정입니다.

### Github-CLI 설치
터미널에서 작업을 하기 위해선 먼저 Github-CLI를 설치해야합니다.

그 전에 레포지토리로 사용할 폴더를 만들어주세요.

여기선 'MyProject'로 해보겠습니다.

``` bash
# 현재 경로 아래에 MyProject 생성
mkdir MyProject

# 해당 폴더로 이동
cd MyProject

# git 연결
git init
```

이제 본격적으로 설치해봅시다.

``` bash
# GitHub CLI 설치 (처음 설치 시)
sudo apt install gh -y
```

### GitHub 계정 연결


``` bash
# 로그인
gh auth login

# 새 레포지토리 생성
gh repo create MyProject --public --source=. --remote=origin
```




