RUBY Commands
==

### Install
1. Node.js 설치 [https://nodejs.org/en/]
2. 터미널 또는 cmd 창에서 버전을 출력하여 정상적으로 설치되었는지 확인
   ~~~dash
    node -v
    v12.16.2 (# 노드버전)
    npm -v
    6.14.4 (# npm 버전)
   ~~~
3. node-sass 설치
   ~~~dash
    npm install -g node-sass
    node-sass -v

    # 출력화면(버전에 따라 다름)
    node-sass 4.14.1  (Wrapper) [JavaScript]
    libsass   3.5.5 (Sass Compiler) [C/C++]
   ~~~
4. Ruby 설치 [https://rubyinstaller.org/downloads/]
![제목-없음-1](https://user-images.githubusercontent.com/57767002/82867750-55039480-9f66-11ea-83db-1467200047ed.jpg)
   ~~~dash
   # 설치할 버전을 모르고 Ruby를 시작하는 경우 Ruby에서 권장하는 버전으로 시작한다.
   ~~~
5. Sass Install
   ~~~dash
   gem install sass
   ~~~
6. sass 설치 확인(node-sass를 기준)
   ~~~dash
   node-sass -v

   # 출력화면(버전에 따라 다름)
   node-sass       4.14.1  (Wrapper)       [JavaScript]
   libsass         3.5.5   (Sass Compiler) [C/C++]    
   ~~~


### Compile
~~~dash
cd 경로

# 특정 파일을 특정 파일 이름으로 컴파일
# Compile foo.scss to bar.css
node-sass foo.scss > bar.css

# 폴더 내의 모든 파일을 컴파일
# node-sass input-folder-path -o output-folder-path
node-sass src/sass --output dist/css
~~~

### Style
1. nested: sass 형식과 유사한 스타일. 기본값 옵션을 추가하지 않아도 기본으로 적용된다.
    ~~~dash
    node-sass --output-style nested src/sass --output dist/css
    ~~~

2. expanded: 표준적인 css 스타일
    ~~~dash
    node-sass --output-style expanded src/sass --output dist/css
    ~~~

3. compact: 여러 룰셋을 한 줄로 나타내는 스타일
    ~~~dash
    node-sass --output-style nested src/sass --output dist/css
    ~~~

4. compressed: 가능한 빈공간이 없는 압축된 스타일
    ~~~dash
    node-sass --output-style compressed src/sass --output dist/css
    ~~~

### watch
watch command는 scss 파일의 변경을 감지하여 변경될 때마다 scss 파일을 컴파일하여 css 파일을 자동 업데이트한다.


디렉터리 단위 또는 파일 단위의 모니터링이 가능하다.

1. 파일 단위 watch
    ~~~dash
    cd 경로

    # watch src/sass/foo.scss -> dist/css
    node-sass --watch src/sass/foo.scss --output dist/css
    ~~~

2. 디렉터리 단위 watch
    ~~~dash
    cd 경로

    # watch src/sass -> dist/css
    node-sass --watch src/sass --output dist/css
    ~~~

### Sass Grammar
+ SassScript [https://poiemaweb.com/sass-script]
+ Sass CSS Extensions [https://poiemaweb.com/sass-css-extention]
+ Sass Built-in Function [https://poiemaweb.com/sass-built-in-function]


### Reference
+ Sass [https://sass-lang.com/]
+ Sassmeister: sass to css converter [https://www.sassmeister.com/]
+ node-sass [https://github.com/sass/node-sass]
+ Libsass [https://github.com/sass/libsass]
