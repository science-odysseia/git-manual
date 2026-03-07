# 1. Git 시작

### 1. Git의 특장점
1. 변경점 관리: 어떤 내용을 누가 어느 시점에 작성했는지 확인할 수 있게 해준다.
2. 버전 관리: 특정 시점에 tag를 달아 버전을 표시해주고, branch 등으로 동시에 여러 버전을 개발할 수 있게 해준다.
3. 백업 & 복구: 프로그램에 문제가 발생했을 때 특정 시점으로 백업이 가능하게 해주고, 자료가 전부 소실되어도 복구할 수 있게 해준다.
4. 협업: 같이 일하는 사람들에게 수정사항을 쉽게 공유할 수 있게 해준다.

### 2. Git 설치하기
# 우분투 기준
`sudo apt-get install git-core`

### 3. Git 프로필 작성하기
```bash
git config --global user.name <"username">
git config --global user.email <"user-email">
```
### 4. Git 최상위 브랜치 이름 설정
# git 저장소를 처음 생성하면 브랜치 이름을 "main"으로 지정함
`git config --global init.defaultBranch <"main">`

# 2. 원격 저장소(Github) 기초

### 1. 개인 액세스 토큰 생성
- 개인 저장소(레포지토리)에 git 작업물을 업로드할 때 필요
- 2023년 이후로는 ID / PW 입력 인증이 불가능하므로 **개인 액세스 토큰(PAT)** 필수
- GitHub 경로: Settings → Developer settings → Personal access tokens → Generate new token
- 토큰 생성 시 **Expiration(만료 기간)** 설정
- ⚠️ **주의:** 토큰은 최초 생성 시에만 전체 값이 보이므로 백업 필수

# git 계정 설정
git config --global user.email "자신의 GitHub email"
git config --global user.name "자신의 GitHub name"

### 2. GitHub 레포지토리 생성 및 연결
1. GitHub에서 새 레포지토리 생성
2. **HTTPS 방식** 선택

echo "# 레포지토리 이름" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin "레포지토리 주소"
git push -u origin main

# 참고
git remote add origin "레포지토리 주소"
git remote set-url origin "레포지토리 주소"
git config --global credential.helper store

# 3. GitHub 업로드해보기

### 2-1. 현재 상태 확인
git status
git add .
git add "파일명"

### 2-2. 불필요한 파일/폴더 무시 (.gitignore)
git reset
sudo nano .gitignore

# 예시
secret.txt
*.log
node_modules/
.env
!important.log

### 4. 원격 저장소에서 레포지토리 받아오기
git clone "<레포지토리>"
git pull

# 3. Git 브랜치

### 1. 브랜치란?
- 기존 코드(master)에 영향을 주지 않고 개별 인원이 작업 가능한 독립적인 공간

### 2. 브랜치 기본 동작
git branch "브랜치명"
git checkout "브랜치명"
git switch "브랜치명"
git checkout -b "브랜치명"
git switch -c "브랜치명"
git branch -d "브랜치명"
git branch -D "브랜치명"
git branch
git branch -m "브랜치명" "바꿀 브랜치명"

git add <파일명>
git add .
git restore --staged <파일명>
git restore --staged .
git reset
git status
git commit -m "메시지"

### 3. 브랜치 합치기
git merge "브랜치명"
git rebase "브랜치명"

### 4. 브랜치 충돌
# 예제는 생략

git add test.txt
git commit -m "Conflict 해결: 두 언어 모두 환영하도록 수정"

# 4. Git Staging
git add .
git add "파일명"

# git add -p 사용법
# y: 추가, n: 추가안함, q: 종료, s: 더 작은 단위, e: 수동 수정

# git stash
# 급하게 다른 브랜치로 넘어갈 때 임시 저장

# 5. Commit 전략
# 기본 전략, 메시지 작성 요령, 변경 사항 확인, 수정, 이력 수정 등

# 6. Git Clean
# 추적하지 않는 파일 삭제

# 7. Git Restore
# commit하지 않은 변경사항 되돌리기

# 8. Git reflog
# reset 등으로 사라진 커밋 히스토리 확인

# 6. Git tag
# Tag란, 종류, 사용법, 브랜치명 vs 태그명 push 비교
