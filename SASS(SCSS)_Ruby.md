SASS(SCSS)사용하기_Ruby
==
~~~
** 사진은 cmd창이지만, 아래의 같은 방법은(순서는) 에디터와 상관없이 공통으로 사용 가능하다. **
~~~

### Install
1. Ruby Installer 설치 [https://rubyinstaller.org/downloads/]

   ~~~bash
   # 설치할 버전에 대해 모를 때는 Ruby에서 권장하는 버전을 다운받는 것을 추천
   # 설치 페이지에서 현재 안정적인 버전을 권장(추천)해준다. (2020.05.29 기준 Ruby + Devkit 2.6.X (x64) 권장)
   # 설치할 때 낮은 버전에서는 PATH를 체크하여 연결
   # 이미 사용 중인 툴이 있다면 설치 중 [msys development toolchain]은 굳이 체크하지 않아도 되며, 
   # 마지막에 한 번 더 체크박스가 있으니 나중에 설치해도 무관
   ~~~
   ![r01](https://user-images.githubusercontent.com/57767002/83221435-c767b500-a1b0-11ea-938c-0f7ca6b71edc.jpg)
   
   ![r07](https://user-images.githubusercontent.com/57767002/83221728-87ed9880-a1b1-11ea-96f4-9dbc73ee1375.jpg)
   
2. Ruby 버전 확인 (필수 X)

   ~~~bash
   ruby -v
   ruby --version
   ~~~
   ![r08](https://user-images.githubusercontent.com/57767002/83222698-e3b92100-a1b3-11ea-820c-503f77cd8098.jpg)
   
3. Sass 설치

   ~~~bash
   gem install sass
   # 명령어를 실행할 때 엑세스 허용여부 창이 뜨면 허용
   
   gem sources -r https://rubygems.org/
   gem sources -a http://rubygems.org/
   # 일부 PC에서 에러가 발생하는 경우 위의 명령어 중 하나를 선택해 입력 후 다시 [gem install sass]
     [회복맨 블로그 참조](https://recoveryman.tistory.com/276)
   ~~~
   ![r09](https://user-images.githubusercontent.com/57767002/83222699-e4ea4e00-a1b3-11ea-9386-71711c1cd97f.jpg)
   
4. Sass 버전 확인(필수 X)

   ~~~bash
   sass -v
   sass --version
   ~~~
   ![r10](https://user-images.githubusercontent.com/57767002/83222700-e582e480-a1b3-11ea-9dcc-b5b61dab1ebd.jpg)
   
5. compile

   ~~~bash
   # sass [경로/컴파일할 파일경로.확장자] [경로/컴파일될 파일경로.확장자]
   ~~~
  ![r20](https://user-images.githubusercontent.com/57767002/83377696-64288d80-a411-11ea-826f-26b67ff16cf7.jpg)

6. 저장하기

   ~~~bash
   Crtl + S
   
   # compile 시 잘못된 부분이 있다면 error가 뜨면서 그 부분을 알림
   ~~~
   ![r16](https://user-images.githubusercontent.com/57767002/83368781-100fb000-a3f5-11ea-819e-0a95a6ffe09e.jpg)
   
   ![r19](https://user-images.githubusercontent.com/57767002/83369983-f83a2b00-a3f8-11ea-9750-b4dd775d87b8.jpg)

7. 작업 끝내기

   ~~~bash
   Ctrl + c
   
   # 작업을 끝내면 터미널 입력창이 다시 나타난다.
   ~~~
   ![r17](https://user-images.githubusercontent.com/57767002/83368621-806a0180-a3f4-11ea-8223-a60e2ac76322.jpg)
   
### Commands 
1. Style
   
   + nested: sass 형식과 유사한 스타일. 기본값 옵션을 추가하지 않아도 기본으로 적용.
   
     ~~~bash
     # sass --style nested [경로/컴파일할 파일명.확장자] [경로/컴파일될 파일명.확장자]
     sass --style nested common.scss common.css
     ~~~

   + expanded: 표준적인 css 스타일
   
     ~~~bash
     # sass --style expanded [경로/컴파일할 파일명.확장자] [경로/컴파일될 파일명.확장자]
     sass --style nested common.scss common.css
     ~~~

   + compact: 여러 룰셋을 한 줄로 나타내는 스타일
   
     ~~~bash
     # sass --style compact [경로/컴파일할 파일명.확장자] [경로/컴파일될 파일명.확장자]
     sass --style nested common.scss common.css
     ~~~

   + compressed: 가능한 빈공간이 없는 압축된 스타일
   
     ~~~bash
     # sass --style compressed [경로/컴파일할 파일명.확장자] [경로/컴파일될 파일명.확장자]
     sass --style nested common.scss common.css
     ~~~
   
     ![r13](https://user-images.githubusercontent.com/57767002/83368682-adb6af80-a3f4-11ea-9add-f49a42831ced.jpg)
     
2. watch: scss 파일의 변경을 감지하여 변경될 때마다 scss 파일을 컴파일하여 css 파일을 자동 업데이트

   + 파일 단위 watch
   
     ~~~bash
     cd 작업경로

     # sass --watch [경로/컴파일할 파일명.확장자]:[경로/컴파일될 파일명.확장자]
     sass --watch src/sass/common.scss dist/css/common.css
     ~~~
     ![r18](https://user-images.githubusercontent.com/57767002/83369984-f96b5800-a3f8-11ea-8e70-239657eb7980.jpg)
  
  + 디렉토리 단위 watch
  
     ~~~bash
     cd 작업경로

     # sass [경로/컴파일할 폴더]:[경로/컴파일될 폴더]
     sass --watch src/sass:dist/css
     ~~~
     ![r14](https://user-images.githubusercontent.com/57767002/83368665-9972b280-a3f4-11ea-86cd-63060a3117d3.jpg)
  
3. style + watch 동시에 명령하기

   ~~~bash
   # sass --watch --style compressed [경로/컴파일할 파일명.확장자] [경로/컴파일될 파일명.확장자]
   sass --watch --style nested common.scss common.css
   ~~~
   ![r15](https://user-images.githubusercontent.com/57767002/83368600-66302380-a3f4-11ea-8f2b-1107d9721ea3.jpg)

  

### Sass Syntax
+ SassScript [https://poiemaweb.com/sass-script]
+ Sass CSS Extensions [https://poiemaweb.com/sass-css-extention]
+ Sass Built-in Function [https://poiemaweb.com/sass-built-in-function]


### Reference
+ Sass [https://sass-lang.com/]
+ Sassmeister: sass to css converter [https://www.sassmeister.com/]
+ node-sass [https://github.com/sass/node-sass]
+ Libsass [https://github.com/sass/libsass]
