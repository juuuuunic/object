Git을 이용한 프로젝트 관리
==

### git 처음 설정하는 컴퓨터(or laptop)
__1.__ 깃허브 패키지 설치
>> ![atom02](https://user-images.githubusercontent.com/57767002/82638296-9122b680-9c41-11ea-91d9-81d08f5e3dab.PNG)
~~~
# git-plus(akonwi)
# 설치 후 Setting의 아래 명령어(Command) 모음을 볼 수 있음
# Pakages > Toggle git tab 또는 Ctrl+Shift+9를 누르면 오른쪽에 패널이 뜬다.
~~~
__2.__ 터미널 또는 cmd 창에서 내 계정 설정하기
>> ![git01](https://user-images.githubusercontent.com/57767002/82781498-e7d3fe80-9e94-11ea-8c41-a8473eb7acfc.png)
~~~bash
git config --global user.email "깃허브 가입 이메일"
git config --global user.name "깃허브 가입 이름"

# cmd창 열기 [winddow+R]
# C드라이브 [c:]
# D드라이브 [d:]
# 폴더 이동하기 [cd 폴더이름]
~~~
__3.__ 깃허브 패키지를 열고 오른쪽 패널에서 작업폴더 및 파일선택, repo 생성
>> ![git0](https://user-images.githubusercontent.com/57767002/82781553-0d610800-9e95-11ea-91a2-454795468963.png)

__4.__ 작업폴더 경로 확인 후 init
>> ![git02](https://user-images.githubusercontent.com/57767002/82781635-47caa500-9e95-11ea-8a1e-be9ba47b4943.png)

__3.__ 작업폴더에 .git 폴더가 생성됐는지 확인
>> ![git06](https://user-images.githubusercontent.com/57767002/82782630-bf013880-9e97-11ea-85c7-123f50651ca1.png)
~~~bash
# .git 디렉토리는 숨김폴더이기 때문에 '숨김 항목'를 설정해주어야 볼 수 있다.
~~~
__4.__ 터미널 또는 cmd창에서 repo 경로 넣기
>> ![git09](https://user-images.githubusercontent.com/57767002/82772075-03311080-9e79-11ea-859b-ddd5d088035c.png)
>> ![git07](https://user-images.githubusercontent.com/57767002/82784146-e60d3980-9e9a-11ea-96f2-5e6539426bfe.png)
~~~bash
git remote add origin https://github.com/경로
# 레파지토리 생성할 때 같이 생성된다.
~~~
__5.__ 리모트 확인(필수 X)
>> ![git08](https://user-images.githubusercontent.com/57767002/82784148-e73e6680-9e9a-11ea-8190-240679731cea.png)
~~~bash
git remote -v
# repo 경로와 같은 주소가 나와야 한다.
~~~
__6.__ stage
>> ![git11](https://user-images.githubusercontent.com/57767002/82785002-b3644080-9e9c-11ea-885a-deb0ad08765e.png)
~~~bash
# 깃허브 패키지에서 commit할 파일 및 폴더 선택 후 Stage All 또는 오른쪽 클릭 stage
# Unstaged Changes 에서 Staged Changes로 이동한다.
~~~
__7.__ commit
>> ![git12](https://user-images.githubusercontent.com/57767002/82785701-160a0c00-9e9e-11ea-8045-594c42cfaeb4.png)
~~~bash
# 1. 커밋할 파일 및 폴더를 선택 후 Staged Changes 아래 입력창에 커밋메세지 작성
# 1-1. Ctrl + Enter
# 1-2. Create Datached commit을 누른다.
~~~
__8.__ push
>> ![git13](https://user-images.githubusercontent.com/57767002/82786012-b2341300-9e9e-11ea-802d-7d9ccbda7346.png)
~~~bash
# 깃허브 패키지
툴의 가장 오른쪽 하단에 있는 Publish를 오른쪽 클릭, Push 선택 
~~~
>> ![git14](https://user-images.githubusercontent.com/57767002/82786300-4ef6b080-9e9f-11ea-969b-15cf39730eb8.png)
~~~bash
# 터미널 또는 cmd 창
git push -u origin master
~~~
__9.__ repo 화면을 새로고침하면 레파지토리가 생성된 것을 확인할 수 있다.
__10.__ 이후 repo를 생성한 작업은 [commit]과 [push]만 반복해주면 된다.

### git 이미 설정된 컴퓨터(or laptop)
*요약: git 처음 설정하는 방법에서 1번과 2번을 빼면 된다.*

__1.__ 깃허브 패키지를 열고 오른쪽 패널에서 작업폴더 및 파일선택, repo 생성
>> ![git0](https://user-images.githubusercontent.com/57767002/82781553-0d610800-9e95-11ea-91a2-454795468963.png)

__2.__ 작업폴더 경로 확인 후 init
>> ![git02](https://user-images.githubusercontent.com/57767002/82781635-47caa500-9e95-11ea-8a1e-be9ba47b4943.png)

__3.__ 작업폴더에 .git 폴더가 생성됐는지 확인
>> ![git06](https://user-images.githubusercontent.com/57767002/82782630-bf013880-9e97-11ea-85c7-123f50651ca1.png)
~~~bash
# .git 디렉토리는 숨김폴더이기 때문에 '숨김 항목'를 설정해주어야 볼 수 있다.
~~~
__4.__ 터미널 또는 cmd창에서 repo 경로 넣기
>> ![git09](https://user-images.githubusercontent.com/57767002/82772075-03311080-9e79-11ea-859b-ddd5d088035c.png)
>> ![git07](https://user-images.githubusercontent.com/57767002/82784146-e60d3980-9e9a-11ea-96f2-5e6539426bfe.png)
~~~bash
git remote add origin https://github.com/경로
# 레파지토리 생성할 때 같이 생성된다.
~~~
__5.__ 리모트 확인(필수 X)
>> ![git08](https://user-images.githubusercontent.com/57767002/82784148-e73e6680-9e9a-11ea-8190-240679731cea.png)
~~~bash
git remote -v
# repo 경로와 같은 주소가 나와야 한다.
~~~
__6.__ stage
>> ![git11](https://user-images.githubusercontent.com/57767002/82785002-b3644080-9e9c-11ea-885a-deb0ad08765e.png)
~~~bash
# 깃허브 패키지에서 commit할 파일 및 폴더 선택 후 Stage All 또는 오른쪽 클릭 stage
# Unstaged Changes 에서 Staged Changes로 이동한다.
~~~
__7.__ commit
>> ![git12](https://user-images.githubusercontent.com/57767002/82785701-160a0c00-9e9e-11ea-8045-594c42cfaeb4.png)
~~~bash
# 1. 커밋할 파일 및 폴더를 선택 후 Staged Changes 아래 입력창에 커밋메세지 작성
# 1-1. Ctrl + Enter
# 1-2. Create Datached commit을 누른다.
~~~
__8.__ push
>> ![git13](https://user-images.githubusercontent.com/57767002/82786012-b2341300-9e9e-11ea-802d-7d9ccbda7346.png)
~~~bash
# 깃허브 패키지
툴의 가장 오른쪽 하단에 있는 Publish를 오른쪽 클릭, Push 선택 
~~~
>> ![git14](https://user-images.githubusercontent.com/57767002/82786300-4ef6b080-9e9f-11ea-969b-15cf39730eb8.png)
~~~bash
# 터미널 또는 cmd 창
git push -u origin master
~~~
__9.__ repo 화면을 새로고침하면 레파지토리가 생성된 것을 확인할 수 있다.
__10.__ 이후 repo를 생성한 작업은 [commit]과 [push]만 반복해주면 된다.

## git clone
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
4. cmd 창에서 생성한 폴더의 경로에 들어간다.
5. 명령어를 실행한다.
>> ![git16](https://user-images.githubusercontent.com/57767002/82788921-5ec4c380-9ea4-11ea-8e47-c50c2885fc1f.png)

