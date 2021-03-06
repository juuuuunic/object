SASS(SCSS)사용하기_Node-sass
==
~~~
** 사진은 Visual Studio Code의 터미널이지만, 아래의 같은 방법은(순서는) 에디터와 상관없이 공통으로 사용 가능하다. **
~~~

### Install
1. Node.js 설치 [https://nodejs.org/en/]

2. Node.js 확인(필수 X)

   ~~~bash
   node -v
   npm -v
   npm list
   npm list -g

   # node.js를 설치하면 npm은 자동으로 설치
   ~~~
   
   ![01](https://user-images.githubusercontent.com/57767002/82981843-da02b280-a027-11ea-8fe9-9a0ce5956621.jpg)
   
3. node-sass 설치

   ~~~bash
    npm install -g node-sass
   ~~~
   
   ![02](https://user-images.githubusercontent.com/57767002/82981844-da9b4900-a027-11ea-834e-f3bc528e1384.jpg)
   
4. node-sass 확인(필수 X)

   ~~~bash
    node-sass -v
   ~~~
   
   ![03](https://user-images.githubusercontent.com/57767002/82981846-da9b4900-a027-11ea-9b0a-11ea9ca46067.jpg)
   
5. compile

   + 파일 단위 compile

     ~~~bash
     cd 작업경로

     # 폴더 내 특정 파일을 특정 파일 이름으로 compile
     # node-sass [경로/컴파일할 파일이름.확장자] > [경로/컴파일될 파일이름.확장자]
     node-sass src/sass/common.scss > dist/css/common.css
     ~~~
     
     ![a](https://user-images.githubusercontent.com/57767002/83382364-e7e87700-a41d-11ea-94c3-cc8435aecad1.jpg)

   + 디렉토리 단위 compile

     ~~~bash
     cd 작업경로

     # 폴더 내의 모든 파일 compile
     # node-sass [경로/컴파일할 파일이 들어있는 폴더명] [경로/컴파일될 파일이 들어있는 폴더명]
     node-sass src/sass --output dist/css
     ~~~
     
     ![s](https://user-images.githubusercontent.com/57767002/83384306-fa64af80-a421-11ea-936b-fc78e642d6ca.jpg)

6. 저장하기
   
   ~~~bash
   Crtl + S
   
   # compile 시 잘못된 부분이 있으면 error의 원인을 알려준다.
   ~~~
   ![k](https://user-images.githubusercontent.com/57767002/83383742-b3c28580-a420-11ea-8a5d-b58a7e38d025.jpg)
   
   ![h](https://user-images.githubusercontent.com/57767002/83382380-f040b200-a41d-11ea-8069-0ae9f07cbbfe.jpg)


7. 작업 끝내기

   ~~~bash
   Ctrl + c
   
   # 작업을 끝내면 터미널 입력창이 다시 나타난다.
   ~~~
   
   ![j](https://user-images.githubusercontent.com/57767002/83382602-6e04bd80-a41e-11ea-8af0-92645f16131f.jpg)
   
### Commands 
1. Style

   + nested: sass 형식과 유사한 스타일. 기본값 옵션을 추가하지 않아도 기본으로 적용

     ~~~bash
     node-sass --output-style nested src/sass --output dist/css
     ~~~

   + expanded: 표준적인 css 스타일

     ~~~bash
     node-sass --output-style expanded src/sass --output dist/css
     ~~~

   + compact: 여러 룰셋을 한 줄로 나타내는 스타일

     ~~~bash
     node-sass --output-style compact src/sass --output dist/css
     ~~~

   + compressed: 가능한 빈공간이 없는 압축된 스타일

     ~~~bash
     node-sass --output-style compressed src/sass --output dist/css
     ~~~

     ![82981839-d96a1c00-a027-11ea-86b9-b3a3bc5ee799](https://user-images.githubusercontent.com/57767002/83384552-77902480-a422-11ea-8aa1-33ae0971b890.jpg)
  
2. watch: scss 파일의 변경을 감지하여 변경될 때마다 scss 파일을 컴파일하여 css 파일을 자동 업데이트

   + 파일 단위 watch

     ~~~bash
     cd 작업경로

     # node-sass --watch [scss 파일경로/파일이름.scss] --output [css 파일경로/파일이름.css]
     node-sass --watch src/sass/파일이름.scss --output dist/css
     ~~~
     
     ![f](https://user-images.githubusercontent.com/57767002/83383505-39920100-a420-11ea-9a8e-b9274156b709.jpg)

   + 디렉토리 단위 watch

     ~~~bash
     cd 작업경로

     # node-sass --watch watch [경로/컴파일할 폴더이름] --output [경로/컴파일될 폴더이름]
     node-sass --watch src/sass --output dist/css
     ~~~
     ![d](https://user-images.githubusercontent.com/57767002/83383510-3a2a9780-a420-11ea-9db0-bc448f5ffd30.jpg)
     
  
### ERROR
  ~~~bash
  # --watch 후 저장을 하면 한 번에 complie 되지 않고 몇 번의 에러 후 진행
  # 에러에 대해서는 추후 추가 예정(2020.05.27 기준)
  ~~~
  ![07](https://user-images.githubusercontent.com/57767002/82981842-da02b280-a027-11ea-9127-cebcc0808872.jpg)
  
  ~~~bash
  # 해결 방법: [C드라이브 \ Users \ (사용자명) \ AppData \ Roaming \ npm \ node_modules \ node-sass \ lib \ render.js] 
  #            버전 교체 (2020.06.01 기준)
  ~~~
  __[해결방법 보러가기](https://github.com/sass/node-sass/issues/1894#issuecomment-390199128)__
  
  ![제목-없음-2](https://user-images.githubusercontent.com/57767002/83376278-b6b37b00-a40c-11ea-8c2c-89f3f5e6f1cf.jpg)




### Sass Syntax
+ SassScript [https://poiemaweb.com/sass-script]
+ Sass CSS Extensions [https://poiemaweb.com/sass-css-extention]
+ Sass Built-in Function [https://poiemaweb.com/sass-built-in-function]


### Reference
+ Sass [https://sass-lang.com/]
+ Sassmeister: sass to css converter [https://www.sassmeister.com/]
+ node-sass [https://github.com/sass/node-sass]
+ Libsass [https://github.com/sass/libsass]
