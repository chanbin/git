# git 사용법

```bash
## 기본 설정 - 기존 프로젝트가 없을 때
1. git program 설치
2. github 홈페이지에서 새로운 repository 생성(기존에 있을 경우 스킵)
3. 바탕화면에 새로운 폴더 만들기
4. 원하는 프로젝트 다운로드(초록색 버튼-clone or download-download zip 하여 3번 폴더에 압축 풀어주기\
   (xxx-master폴더 안의 내용만 풀어주세요)
5. cmd창을 켜고, 해당 폴더로 이동
6. git init
7. git remote add origin <깃허브repository주소>.git\
8. git config --global user.email "<본인깃헙계정 로그인아이디>"

## 기본 설정 - 기존 프로젝트가 있을 때(예지)
1. git program 설치
2. 바탕화면에 새로운 폴더 만들기
3. cmd창을 켜고, 해당 폴더로 이동
4. git init
5. git remote add origin <깃허브repository주소>.git\
6. git config --global user.email "<본인깃헙계정 로그인아이디>"
7. git pull origin master --> 저장소에 내용을 로컬로 가져오기
```
<br>

<중요!>깃허브 `홈페이지`에서 코드 수정을 했다면, 수정한 내용을 반드시 로컬 폴더로 가져와야한다.<br>git pull origin master

```bash
## 파일 생성 또는 수정, 삭제 후 git에 올리기
1. cmd창을 켜고, 해당 폴더로 이동
2. git add *
3. git commit -m "본인이 하고 싶은 코멘트"
4. git push origin master

```

# Jekyll


# 잡하단 것들

git init 으로 새로운 로컬저장소 만들기\
git remote add <원격지이름> <원격서버주소>.git\
git remote add origin https://github.com/chanbin/xxx.git

git add <파일 이름> *로 한번에 인덱스에 넣을 수 있다\
git commit -m "설명" 인덱스에서 헤드(로컬최종장소)로 넘긴다\
git push <원격지> <브랜치> 헤드내용이 깃헙으로 올라감\
git push -f <원격지> <브랜치> push 실패 시, 강제로 push (local로 git clone시 README.md 파일이 있으면 push가 안됨)\
git push origin master

git rm -rf <Directory> 레포에서 디렉터리 지우기\
git commmit -m "디렉토리 삭제"\
git push origin master
  
git pull origin master 로컬에서 수정하면 pull\
git push origin master

git clone 은 깃헙에서 로컬로 가져오기

clone 후 pull로 병합 할 때 fatal: refusing to merge unrelated histories\
git pull origin master --allow-unrelated-histories


# 파일 지우기
git init 과 git remote add <원격지이름> <원격서버주소>.git을 해야한다\
[추가] git config --global user.email "you@example.com"로 계정 설정을 해야한다.

git rm file.txt 파일 삭제\
git commit -m "remove file.txt" 커밋\
git push <원격지> <브랜치> 푸시

git rm --cached file.txt => 레포에서만 지우기, 로컬에는 남음(나중에는 gitignore 파일에 설정해야 편함)\

jekyll new [web-site]\
gem install bundler\
bundle install\
bundle exec jekyll build\
bundle exec jekyll serve\
