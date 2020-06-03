SASS(SCSS)사용하기_Koala
==
~~~
** 사진은 Atom이지만, 아래의 같은 방법은(순서는) 에디터와 상관없이 공통으로 사용 가능하다. **
~~~

### Install
1. koala Installer 설치 [http://koala-app.com/]

   ![koala-sass-compiler](https://user-images.githubusercontent.com/57767002/83590471-cbb91700-a590-11ea-9ef9-02e12d77f4c7.jpg)

   ![01](https://user-images.githubusercontent.com/57767002/83588631-c78afa80-a58c-11ea-9c8d-0efb0f29fc6a.jpg)

   ![02](https://user-images.githubusercontent.com/57767002/83588632-c8bc2780-a58c-11ea-9d00-8561a864c0f1.jpg)
   
2. compile시 필요값 설정

   + __Source map:__ sass(scss)를 css로 컴파일 시킬 때 서로 연결시켜주는 코드이기 때문에 생성 후 계속 유지
   
   + __Autoprefix:__ 밴더 프리픽스(Vendor Prefix) 자동 생성
     ~~~bash
     # VS Code와 마찬가지로 Koala 또한 필요에 따라 접두사(prefix)를 추가하기 때문에 css마다 다를 수 있다.
     ~~~
     
   + __Output Style__: 원하는 css 스타일
     ~~~bash
     1. nested: sass 형식과 유사한 스타일. 기본값 옵션을 추가하지 않아도 기본으로 적용
     2. expanded: 표준적인 css 스타일
     3. compact: 여러 룰셋을 한 줄로 나타내는 스타일
     4. compressed: 가능한 빈공간이 없는 압축된 스타일
     ~~~
     
     ![03-1](https://user-images.githubusercontent.com/57767002/83588633-c8bc2780-a58c-11ea-9cd1-7877a2793641.png)
   
3. 사용하는 툴에서 작업폴더 열기

   ~~~bash
   # 폴더를 드래그해 가지고 오는 것도 가능하다.
   ~~~
   
   ![05-1](https://user-images.githubusercontent.com/57767002/83589801-5d278980-a58f-11ea-90ea-d4baf08ca87f.png)
   
4. compile

   ~~~bash
   # 작업하고 있는 파일을 클릭하면  오른쪽에 패널에서 하단에 있는 complie을 클릭...!
   ~~~
   
   ![06](https://user-images.githubusercontent.com/57767002/83588649-cfe33580-a58c-11ea-80ee-dc4d399133c7.jpg)
   
   ![06-1](https://user-images.githubusercontent.com/57767002/83589712-41bc7e80-a58f-11ea-84f7-314886aba4a5.png)
   
5. css/css.map 확인

   ~~~bash
   # 위에서 언급한 것과 같이 css.map은 sass(scss)와 css를 연결시켜주는 코드이기 때문에 생성 후 계속 유지해야 한다.
   # 필요에 따라 접두사(prefix)를 추가하는 점을 주의하며, css 하단에 sass(scss)와 연결되어있는 URL을 확인할 수 있다.
   ~~~
   
   ![10](https://user-images.githubusercontent.com/57767002/83588660-d5408000-a58c-11ea-990f-510678cb06e5.jpg)

7. 작업 끝내기

   ~~~bash
   # 그냥 끄면 된다.
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
