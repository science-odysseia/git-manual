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
github 파일들은 온라인, 내 파일들은 오프라인에 있습니다.

이 둘을 연결하기 위한 보안 조치를 하나 만들어줘야 합니다.

우리는 `SSH`를 이용해서 연결해 보려고 합니다.

**`ssh-keygen`을 통해 SSH 키를 생성하고 GitHub에 등록하는 과정은 처음 1회만 하면 됩니다.**

먼저 SSH키를 생성해보겠습니다.

``` bash
ssh-keygen
```

만약 없다는 오류메세지가 뜨면, 아래 명령어로 설치해줍시다.

``` bash
sudo apt update
sudo apt install openssh-client
```

`ssh-keygen`을 실행하면 아래 항목들이 한 줄씩 뜰 텐데, 모두 엔터를 쳐 줍시다.

이 경우 저장된 경로를 기억해주세요. 이 키를 나중에 사용할 것입니다.

혹은 아래처럼 직접 경로를 입력해도 됩니다. 

다만 리눅스와 다르게 ~를 홈 디렉토리로 인식하지 않으니, 경로를 풀어주세요.

또한 경로를 지정할 땐 경로상 모든 폴더가 이미 존재해야 합니다. 미리 만들고 해주세요.

~~랜덤하게 다 바꿔놨으니까 해킹할 생각은 접어라~~

    Enter file in which to save the key (/home/scienceodysseia/.ssh/id_ed25519): /home/user/MyProject/.ssh/id_ed25519
    Enter passphrase (empty for no passphrase): 
    Enter same passphrase again: 
    Your identification has been saved in /home/user/MyProject/.ssh/id_ed25519
    Your public key has been saved in /home/user/MyProject/.ssh/id_ed25519.pub
    The key fingerprint is:
    SHA256:************ user@linux
    The key's randomart image is:
    +--[ED25519 256]--+
    |   .o+*B+.       |
    |  . =O+=+o.      |
    |   .o.=o..       |
    |    . o +        |
    |     . S .       |
    |      + .        |
    |     . .         |
    |    .o.          |
    |     E*          |
    +----[SHA256]-----+


위의 경우, `.ssh` 폴더 안에 `id_ed25519` 라는 비밀키와, `id_ed25519.pub`라는 공개키 2개가 생성되어 있을 겁니다.

우리는 `id_ed25519.pub`이라는 공개키를 사용할 것입니다.

생성된 공개키의 내용을 확인해봅시다

``` bash
cat ~/.ssh/id_ed25519.pub
```

`~/.ssh/id_ed25519.pub` 대신 자신이 `id_ed25519.pub`을 저장한 경로를 넣으셔도 됩니다.

    ssh-ed25519 ***************************************** user@BOOK-*********

**나오는 결과 줄 전체를 복사해주세요.**

키를 만들었으면 이제 자신의 계정에 등록을 해야겠죠?

이거도 처음 한번만 하면 됩니다.

1. [Github](https://github.com)에 로그인하세요.
2. 우측 상단에 있는 자신의 아이콘을 누르고, `Settings`에 들어가세요.
3. 왼쪽 목록에 `SSH and GPG keys`에 들어가서, 오른쪽 상단에 `New SSH key`를 누르세요.
4. 
|![GitHub-Settings](githubimgs/github_settings.png)|![GitHub-sshkey](githubimgs/github_sshkey.png)|
|---|---|



``` bash
# 로그인
gh auth login
```

``` bash
# 새 레포지토리 생성
gh repo create MyProject --public --source=. --remote=origin
```




