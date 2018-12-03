# git 사용법

git init 으로 새로운 로컬저장소 만들기<br\>
git remote add <원격지이름> <원격서버주소>.git<br\>
git remote add origin https://github.com/chanbin/xxx.git<br\><br\>

git add <파일 이름> *로 한번에 인덱스에 넣을 수 있다<br\>
git commit -m "설명" 인덱스에서 헤드(로컬최종장소)로 넘긴다<br\>
git push <원격지> <브랜치> 헤드내용이 깃헙으로 올라감<br\>
git push origin master<br\><br\>

git clone 은 깃헙에서 로컬로 가져오기<br\>
