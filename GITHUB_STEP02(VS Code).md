Git을 이용한 프로젝트 관리
==

### git 처음 설정하는 컴퓨터(or laptop)
__1.__ 터미널 또는 cmd 창에서 내 계정 설정하기
>> ![git04](https://user-images.githubusercontent.com/57767002/82773873-24e0c680-9e7e-11ea-863f-2f082825d9b2.png)
~~~bash
git config --global user.email "깃허브 가입 이메일"
git config --global user.name "깃허브 가입 이름"
~~~
__2.__ init
>> ![git16](https://user-images.githubusercontent.com/57767002/82777549-67f46700-9e89-11ea-818a-f036b6a2d21b.png)
~~~bash
git init
# 비어있는 repo가 시작됐다는 메세지와 함께 왼쪽 패널에서 파일 및 폴더 개수가 확인된다.
~~~
__3.__ 작업폴더에 .git 폴더가 생성됐는지 확인
>> ![git06](https://user-images.githubusercontent.com/57767002/82771646-abde7080-9e77-11ea-9fd0-65bc1dab17bd.png)
~~~bash
.git 디렉토리는 숨김폴더이기 때문에 '숨김 항목'를 설정해주어야 볼 수 있다.
~~~
__4.__ repo 경로 넣기
>> ![git09](https://user-images.githubusercontent.com/57767002/82772075-03311080-9e79-11ea-859b-ddd5d088035c.png)
>> ![git07](https://user-images.githubusercontent.com/57767002/82773782-e1865800-9e7d-11ea-8103-f0e598364cf5.png)
~~~bash
git remote add origin https://github.com/경로
# 레파지토리 생성할 때 같이 생성된다.
~~~
__5.__ 리모트 확인(필수 X)
>> ![git08](https://user-images.githubusercontent.com/57767002/82773655-89e7ec80-9e7d-11ea-9ac5-f3d48a988690.png)
~~~bash
git remote -v
# repo 경로와 같은 주소가 나와야 한다.
~~~
__6.__ 왼쪽 패널에서 commit할 파일 및 폴더 선택 후 commit 메세지 작성
>> ![git17](https://user-images.githubusercontent.com/57767002/82777676-c02b6900-9e89-11ea-92d7-093237b6ae02.png)
~~~bash
# 따로 선택하지 않으면 전체가 commit 된다.
~~~
__7.__ commit
>> ![git19](https://user-images.githubusercontent.com/57767002/82778218-b7d42d80-9e8b-11ea-99cb-e293c2b5a28e.png)
~~~bash
1. Crtl + Enter 
2. 왼쪽 패널 오른쪽 상단 ···(기타작업) 오른쪽 클릭 > 모두 커밋
3. 스테이징 메세지가 뜨면 '예'를 선택한다.
~~~
__8.__ stage
>> ![git18](https://user-images.githubusercontent.com/57767002/82778000-ef8ea580-9e8a-11ea-9370-8e7957f8d20a.png)
~~~bash
# stage 이후 왼쪽 패널 상단에 작은 바(-)가 이동하는 것을 볼 수 있다.
~~~
__9.__ push
>> ![git13](https://user-images.githubusercontent.com/57767002/82773474-1b0a9380-9e7d-11ea-859e-f41043f8f469.png)
>> ![git21](https://user-images.githubusercontent.com/57767002/82778460-75f7b700-9e8c-11ea-86a9-72050ee522b3.png)
~~~bash
1. git push -u origin master
2. 왼쪽 패널 오른쪽 상단 ···(기타작업) 오른쪽 클릭 > 푸시
2-1. master 분기 창이 뜨면 '예'를 선택한다.

# 왼쪽 패널은 아무것도 없는 상태이다.
~~~
__10.__ repo 화면을 새로고침하면 레파지토리가 생성된 것을 확인할 수 있다.

### git 이미 설정된 컴퓨터(or laptop)
*요약: git 처음 설정하는 방법에서 1번만 빼면 된다.*

__1.__ init
>> ![git16](https://user-images.githubusercontent.com/57767002/82777549-67f46700-9e89-11ea-818a-f036b6a2d21b.png)
~~~bash
git init
# 비어있는 repo가 시작됐다는 메세지와 함께 왼쪽 패널에서 파일 및 폴더 개수가 확인된다.
~~~
__2.__ 작업폴더에 .git 폴더가 생성됐는지 확인
>> ![git06](https://user-images.githubusercontent.com/57767002/82771646-abde7080-9e77-11ea-9fd0-65bc1dab17bd.png)
~~~bash
.git 디렉토리는 숨김폴더이기 때문에 '숨김 항목'를 설정해주어야 볼 수 있다.
~~~
__3.__ repo 경로 넣기
>> ![git09](https://user-images.githubusercontent.com/57767002/82772075-03311080-9e79-11ea-859b-ddd5d088035c.png)
>> ![git07](https://user-images.githubusercontent.com/57767002/82773782-e1865800-9e7d-11ea-8103-f0e598364cf5.png)
~~~bash
git remote add origin https://github.com/경로
# 레파지토리 생성할 때 같이 생성된다.
~~~
__4.__ 리모트 확인(필수 X)
>> ![git08](https://user-images.githubusercontent.com/57767002/82773655-89e7ec80-9e7d-11ea-9ac5-f3d48a988690.png)
~~~bash
git remote -v
# repo 경로와 같은 주소가 나와야 한다.
~~~
__5.__ 왼쪽 패널에서 commit할 파일 및 폴더 선택 후 commit 메세지 작성
>> ![git17](https://user-images.githubusercontent.com/57767002/82777676-c02b6900-9e89-11ea-92d7-093237b6ae02.png)
~~~bash
# 따로 선택하지 않으면 전체가 commit 된다.
~~~
__6.__ commit
>> ![git19](https://user-images.githubusercontent.com/57767002/82778218-b7d42d80-9e8b-11ea-99cb-e293c2b5a28e.png)
~~~bash
1. Crtl + Enter 
2. 왼쪽 패널 오른쪽 상단 ···(기타작업) 오른쪽 클릭 > 모두 커밋
3. 스테이징 메세지가 뜨면 '예'를 선택한다.
~~~
__7.__ stage
>> ![git18](https://user-images.githubusercontent.com/57767002/82778000-ef8ea580-9e8a-11ea-9370-8e7957f8d20a.png)
~~~bash
# stage 이후 왼쪽 패널 상단에 작은 바(-)가 이동하는 것을 볼 수 있다.
~~~
__8.__ push
>> ![git13](https://user-images.githubusercontent.com/57767002/82773474-1b0a9380-9e7d-11ea-859e-f41043f8f469.png)
>> ![git21](https://user-images.githubusercontent.com/57767002/82778460-75f7b700-9e8c-11ea-86a9-72050ee522b3.png)
~~~bash
1. git push -u origin master
2. 왼쪽 패널 오른쪽 상단 ···(기타작업) 오른쪽 클릭 > 푸시
2-1. master 분기 창이 뜨면 '예'를 선택한다.

# 왼쪽 패널은 아무것도 없는 상태이다.
~~~
__9.__ repo 화면을 새로고침하면 레파지토리가 생성된 것을 확인할 수 있다.

__10.__ 이후 repo를 생성한 작업은 [commit]과 [push]만 반복해주면 된다.

### git clone
+ 다른 프로젝트에 참여하거나(Contribute) git 저장소를 복사하고 싶을 때 사용하는 명령어
+ git clone을 실행하면 프로젝트의 히스토리를 전부 받아오기 때문에 서버의 디스크가 망가져도 클라이언트 저장소를 가져다가 복구할 수 있다.
~~~ bash
git clone 복사한repository주소
~~~
1. 소스를 복사(저장)하고자 하는 경로에 폴더를 만든다. 
2. 복사(저장)하고자 하는 repository를 찾아 [Clone or download] 버튼을 누른다.
>> ![git15](https://user-images.githubusercontent.com/57767002/82788296-2670b580-9ea3-11ea-9337-fd48ba546d52.png)
3. Download ZIP 후 생성한 폴더에 이동시킨다.
3-1. 박스에 뜨는 주소를 복사한다.
4. VS Code에서 생성한 폴더를 연다.
5. 터미널창에서 명령어를 실행한다.
>> ![git16](https://user-images.githubusercontent.com/57767002/82788293-25d81f00-9ea3-11ea-9b51-807e9073f386.png)

