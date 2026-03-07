# Git Settings

## 1. Github 회원가입 / 로그인
1. https://github.com 접속 (이걸 보고 있다면 이미 접속했겠지만......)
2. 계정이 없다면 'Sign up'으로 회원가입, 있다면 Sign in'으로 로그인

|![github_main](githubimgs/github_main.png)|![github_signup](githubimgs/github_signup.png)|
|---|---|

3. Username과 Email은 기억하세요. 나중에 쓰입니다.


## 2. Git 설치
### PS(PowerShell) 버전(Windows)
winget을 이용하여 설치해보겠습니다.

1. 우선 winget이 이미 있는지 확인

``` powershell
winget --version
```

    vx.xx.xx

해당 형식이 나오면 설치된 것.

만약 없다면

``` powershell
Invoke-WebRequest -Uri "https://aka.ms/Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle" -OutFile "$env:TEMP\AppInstaller.msixbundle"
Add-AppxPackage -Path "$env:TEMP\AppInstaller.msixbundle"
```

실행 후 ps 종료 후 재시작. 
