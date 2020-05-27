SASS(SCSS)사용하기_Node-sass
==
~~~
** Visual Studio Code를 통한 터미널 사용을 전제로 한다. **
~~~

### Install
1. Node.js 설치 [https://nodejs.org/en/]
2. Node.js 확인(필수 X)
   ~~~dash
   node -v
   npm -v
   npm list
   npm list -g

   ## node.js를 설치하면 npm은 자동으로 설치된다.
   ~~~
3. node-sass 설치
   ~~~dash
    npm install -g node-sass
   ~~~
4. node-sass 확인(필수 X)
   ~~~dash
    node-sass -v
   ~~~
5. compile
   ~~~dash
   cd 작업경로

   # 특정 파일을 특정 파일 이름으로 컴파일
   # Compile foo.scss to bar.css
   node-sass foo.scss > bar.css

   # 폴더 내의 모든 파일을 컴파일
   # node-sass input-folder-path -o output-folder-path
   node-sass src/sass --output dist/css
   ~~~

### Commands 
1. Style
+ nested: sass 형식과 유사한 스타일. 기본값 옵션을 추가하지 않아도 기본으로 적용.
  ~~~dash
  node-sass --output-style nested src/sass --output dist/css
  ~~~

+ expanded: 표준적인 css 스타일
  ~~~dash
  node-sass --output-style expanded src/sass --output dist/css
  ~~~

+ compact: 여러 룰셋을 한 줄로 나타내는 스타일
  ~~~dash
  node-sass --output-style nested src/sass --output dist/css
  ~~~

+ compressed: 가능한 빈공간이 없는 압축된 스타일
  ~~~dash
  node-sass --output-style compressed src/sass --output dist/css
  ~~~

2. watch: scss 파일의 변경을 감지하여 변경될 때마다 scss 파일을 컴파일하여 css 파일을 자동 업데이트

+ 파일 단위 watch
  ~~~dash
  cd 작업경로

  # watch [scss 파일경로/파일이름.scss] -> [css 파일경로/파일이름.css]
  node-sass --watch src/sass/파일이름.scss --output dist/css
  ~~~
  
+ 디렉토리 단위 watch
  ~~~dash
  cd 작업경로

  # watch [sass 디렉토리 경로] -> [css 디렉토리 경로]
  node-sass --watch sass디렉토리경로 --output css디렉토리경로
  ~~~

### Sass Syntax
+ SassScript [https://poiemaweb.com/sass-script]
+ Sass CSS Extensions [https://poiemaweb.com/sass-css-extention]
+ Sass Built-in Function [https://poiemaweb.com/sass-built-in-function]


### Reference
+ Sass [https://sass-lang.com/]
+ Sassmeister: sass to css converter [https://www.sassmeister.com/]
+ node-sass [https://github.com/sass/node-sass]
+ Libsass [https://github.com/sass/libsass]
