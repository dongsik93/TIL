## Git branch & pull request



### git branch

https://learngitbranching.js.org



- master branch는 터치하지 않고, 업데이트를 해오는 용도로만 master로
- 다른 branch로 add, commit 하기
- merge는 PM만
- branch명은 이름이 아닌, 기능별로 구현하는게 좋음



##### PM

1. django-admin startproject testGit
2. cd testGit
3. touch .gitignore
4. git init : master 브랜치
5. git add .
6. git commit -m 
7. django-admin startapp
8. setting.py 설정
9. git commit -m 
10. (모든사람이 동일하다는 가정, 이제 분업)
11. github 콜라보레이터
12. git remote add origin https://github.com/dongsik93/ourProject.git
13. git push origin master

##### 팀원

1. git clone https://github.com/dongsik93/ourProject.git
2. cd testGit
3. git log



##### 모두같이

1. git branch
2. git branch dongsik
3. git checkout dongsik



##### PM

1. models.py(모두가 반영해야 하는 코드)
2. git add .
3. git commit -m "모델수정"
4. git push origin dongsik (dongsik 브랜치로 올린다)
5. github에` compare & pull request`창이 떠있음 // 아직 모델수정한게 반영이 안되어 있는 상태
6. `compare & pull request` 클릭 후 Write에 내용 작성 후 create pull request
7. `Merge pull request` 버튼 -> `Configm merge` 클릭



##### 팀원

1. git pull origin master : master 브랜치를 가져옴



** 동시에 수정했다는 가정(동시에 pull request)

##### 팀원1

1. git add .
2. git commit -m "column이름 마음에 안들어서 바꿈"
3. git push origin 팀원1



##### 팀원2

1. git add .
2. git commit -m "fix name"
3. git push origin dongsik



각자 pull request 보내기



충돌해결

`resolve conflicts` 클릭 -> 비교 후 선택 -> mark resolve -> commit -> merge pull request



- git pull origin master : 최신 코드 내려 받기