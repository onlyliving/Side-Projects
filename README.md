# (Side Project) Background Image Search Service

자기 개발을 위해 단기 프로젝트로 작업한 내용입니다. 피드백 주시면 감사하겠습니다. ( 문의 메일 : greensohee88@naver.com )



## Getting Started

```
// 원격저장소 코드 다운받기. 다운 받을 폴더에서 터미널로 명령어 실행
git clone https://github.com/onlyliving/Side-Projects.git

// package.json 파일에 작성된 모듈(npm) 모두 설치
npm i

// 웹팩 빌드하기 (webpack.config.js)
npm run build

// dist 파일 열기 dist/index.html
// </body>아래 코드 추가
<script src="index.bundle.js"></script>
```




## Q. 왜 이런 서비스(배경이미지 검색)를 선택했나요?

- 오픈 API를 이용하여, 개인이 단 시간에 할 수 있는 기능이 무엇이 있을까 고민하였습니다.
- 오픈 API를 검색하다가 이미지 데이터를 제공하는 '언스플래쉬 사이트'를 이용해보자 라는 방향을 잡았습니다.

- 아이디어 : 이미지 검색에서 어떤 니즈가 있을까 고민하였습니다. 웹 디자인 업무에서 배경이미지를 찾을 때가 꽤 있습니다. 그걸 생각해서 카드콘텐츠에 들어가는 배경 이미지를 찾게 해주면 좋겠다라는 아이디어가 떠올랐습니다.

- Open API : [언스플래쉬 사이트](https://unsplash.com/developers)



## 구현 기능

### 1. 검색

```
특정 단어 검색, 태그 검색
```

> **태그 종류**
>
> 1. 타 유료이미지 사이트에서 검색되는 태그를 기준으로 검토하였습니다.
> 2. 영어 검색만 되어서, 태그 클릭 시 관련 영단어를 제시하였습니다. (예, #자연 ->  'natural, green' )
> 3. TODO : 현재는 태그를 제 임의로 지정하였는데, 사용자의 니즈를 파악하기 위해서 나중에는 많이 검색한 키워드가 무엇인지도 알 수 있게 하면 좋을 것 같습니다.
>    * 필요한 검색 기능이 있으면 제 메일(greensohee88@naver.com)로 문의주시면 감사하겠습니다. 



### 2. 검색 결과 (중요)

```
카드콘텐츠 배경 이미지를 찾아주는 서비스이므로, 검색 결과를 보여주는 이미지를 배경으로 어둡게 처리하고, 예시 문구를 넣어서 보여줍니다.
```

[검색 결과 참고 링크](https://fonts.google.com/)

>**검색결과 순서**
>
>- 이미지 좋아요(like) 숫자가 높은 순으로 내림차순
>
>**검색결과 필터**
>
>- 이미지 형태에 따라 정사각형(default), 가로형, 세로형 이미지를 선택해서 노출
>
>- 임의로 정한 텍스트 문구를 한번에 바꿀 수 있도록 기능 추가
>
>- 폰트체 설정 기능 추가
>
>검색 결과 이미지 위에 마우스 올릴 때, 이미지 오른쪽 상단에 링크(LINK) 버튼 생성. 링크(LINK) 클릭 시 이미지 관련 페이지로 이동 (다운로드 가능)



## 프로젝트 기간

- 3.23 ~ 3.27, 일주일 
- (추가글) 25일부터 본격적으로 진행

```
3.23 : api 세팅
3.24 : 마크업, css
3.25~26 : js
3.27 : 프로젝트 마무리
```



## 완성된 사이트

[https://onlyliving.github.io/Side-Projects/dist/](https://onlyliving.github.io/Side-Projects/dist/)



## 회고

개인으로 처음 해보는 사이드프로젝트라서 단기 프로젝트로 생각하고 시작하였습니다. 제 목표는 원하는 기능을 제한 시간 안에 완성하는 것이였고, 목표를 달성하여 일단 기분은 좋습니다. 여기에서 더 필요한 기능을 추가하고, 수정해야 될 사항을 체크해서 앞으로도 조금씩 개선할 예정입니다.

과연 '나'는 의미있는 서비스를 구현하였나? 라는 생각이 듭니다. 아직 사용자와 소통을 하지 못해서 이후에 피드백을 받을 수 있도록 조치를 취해야겠습니다.

맥 IOS 디바이스를 기준으로 작업하여서, 브라우저 이슈가 있을 수 있습니다. (아직 체크하지 못함)

목표를 소극적으로 잡았나라는 생각도 듭니다. 성취감은 있지만 너무 하기 쉬운 것을 한 걸까라는 의문이 들어서 다음에는 좀 더 도전적인 프로젝트를 고심해 볼 것 같습니다.