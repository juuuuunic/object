Git 협업하기
==
~~~ bash
# 요약

1. 팀원 중 한 명이 master가 되어 환경설정을 마친 프로젝트 파일을 Github에 올리기
2. 생성한 repository > Setting > Manage access 에서 [Invite a collaborator]
3. 팀원 이메일에 초대장 보내기
4. 초대장을 받은 팀원은 메일에서 [View intitaion] > [Accept invitation]
5. repository > Setting > Manage access 에서 추가된 팀원 확인하기
6. 팀원들은 각각 자신의 PC에서 branch를 생성하여 독립된 작업공간 마련
7. 자신의 branch에 push 할 때는 [git push origin 자신의branch이름]
8. 정상적으로 push가 됐으면, repository에 branch를 선택할 수 있는 박스가 생성됨
7. 병합이 필요할 때 master의 branch에 merge한다.
~~~
branch
--
### master branch
+ git init 할 때 자동으로 생성되는 기본 branch
+ 동료들의 작업내용을 하나로 합칠 때 사용하는 뼈대 branch 또는 배포용 branch로도 사용할 수 있다. branch 전략은 각각 다르다.

### branch Commands
##### branch 생성
```sh
git branch {branch name}
```
+ 새로운 branch를 생성하면, 기반이 되는 branch(merge branch)의 버전을 그대로 복사
+ commit 내용도 복사된 branch와 같음
##### branch 이동
```sh
git checkout {branch name}
```
##### branch를 생성함과 동시에 이동
```sh
git checkout-b {branch name}
```
##### branch 목록 및 현재 사용하고 있는 branch를 확인
```sh
git branch -r : 원격 브랜치 목록
git branch -a : 로컬/원격 모든 브랜치 목록
```
+ *표시가 현재 사용하고 있는 branch
##### branch push
```sh
git checkout master
git merge branchName
git push origin master
```
+ 팀원은 master branch에 push하기 전에 먼저 자신의 repository에 merge한 다음에 master branch에 push
+ master가 아닌 branch에 푸쉬하기 때문에 명령어 주의!
+ 자신의 branch는 최신 코드를 push/pull하는 용도로만 사용하는 것이 관리에 있어서 용이
+ master branch는 관리만
##### master branch에서 pull
```sh
git checkout master
git pull origin master
```
##### 최신코드를 자신의 branch에 이동 후 merge
```sh
git checkout branchName
git merge master
```
##### 이전 코드로 돌아가기
```sh
git revert commitNumber
```
### branch 충돌(conflicts)
##### 기준 branch와 대상 branch가 같은 파일의 같은 부분을 수정할 때 충돌 발생
