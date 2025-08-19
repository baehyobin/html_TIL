# HTML
### 250804 HTML시작
* 비주얼 스튜디오 코드 설치, 깃허브 회원가입, 깃 설치
* 비주얼 스튜디오 환경설정 및 플러그인 설치
### 주의사항
1. 영문 대소문자 사용하기(소문자 권장) 예) subTitle, sub_title
2. 숫자는 영문 뒤로 배치하기 예) sub1, main002
3. 공백 + 한글 사용금지
4. 특수문자 사용금지(#,$,%,^,&,*,(,+,\,~,★ 등..) *언더바(`_`) 하이픈(`-`) 가능
5. 이름은 의미있게 사용하기 예) images, fonts, mail, cafe 등..
6. 비주얼스튜디오코드 실행 시 작업 폴더 연결여부 확인하기
7. (위) 작업폴더 미연결 -> File -> Close Folder 후 다시 File -> Open Folder
### 깃(Git) 설치 확인
* Vscode에서 단축키 `Ctrl+J` 터미널 실행
* `git-v` 깃설치버전 확인(버전결과 나오면 설치OK)
### 터미널 `Ctrl_J` 기본 설정
* 윈도우 기본 터미널 powershell을 git Bash로 변경하기
* (위 gitBash는 깃설치 후 사용 가능)
## git 설정과 gitHub 업로드까지 순서(터미널 입력 기준)
1. `git config --list` : 현재 깃 설정 정보 확인
2. 새로운 값이 입력 안되면 터미널에서 `Ctrl+C` 또는 `Q`
3. 위 1번에서 깃 설정정보에 name, email이 내 정보가 아닐때
4. `git config --global user.email "hyobin9824@gmail.com"` 이메일 설정
5. `git config --global user.name "hyobin9824"` 이름 설정(메일아이디 동일)
6. `git config --list` 위 4~5번 설정 올바르게 됐는지 확인
---
7. `git init` 현재 폴더를 작업 디렉터리 폴더로 연결, 폴더경로 옆에 **master** 표시 생기면 성공!
8. `git branch -M main` 깃 디렉터리 명칭 = 브랜치라 부름. 해당 브랜치명을 개인에 맞게 변경. 기본이 **main**
---
9. `git add .` **.**이란 작업수정한 모든 파일. 모든 파일을 대기소(스테이지)에 올린다는 뜻
10. `git status` 현재 스테이지 확인 명령
11. `git commit -m "기록메세지"` 현재 올리는 파일이 어떤 내용인지 기록
12. `git remote add origin 깃허브저장소주소` 깃허브 저장소 업로드 위치가 어디인지 주소 연결
13. `git push origin main` 11번에서 커밋한 파일을 12번 저장소에 최종 업로드
### 한번만 작성하면 끝인 깃 명령어
* `git config` 이름, 이메일 설정한 것
* `git init` 저장소 설정 
* `git remote add origin` 저장소 주소 설정
### 작업 시 깃허브 업로드를 위해 반복해야하는 깃 명령어
* `git add .`
* `git commit -m "기록 메세지"`
* `git push origin main`
### 중간 확인 시
* `git status` 또는 `git log`
# HTML 작성법
* `<태그 속성="값" 속성="값"></태그>`
* 시작태그부터 닫기태그까지 = 한번에 **요소(element)**로 명칭
* 속성은 시작태그에만 쓰고 닫기태그에는 사용X
* `파일명.html`
* 파일명은 영문대소문자+숫자 조합으로만 작성
* HTML 작성의 시작은 항상 **구조태그**로 해야한다! `html:5`

## Vscode 자주 쓰는 단축키
* `Ctrl+\` 화면 분할
* `Ctrl+K+\` 화면 상하 분할
* `Alt+Z` 줄바꿈
* `Alt+상하 방향키` 줄 이동
* `Shift+Alt+상하방향키` 선택한 줄 복제
* `Shift+Alt+A` 주석생성
## 250805 자주 쓰는 HTML 문서 기본 태그
1. `<h1>~<h6>` block - 1대제목~6소제목
2. `<p>` block - 제목 아래 작성하는 내용 태그
3. `<br>` inline - 내용 안에 작성하는 줄바꿈태그
4. `<em><strong>` inline - 내용 안 강조태그
5. `<del>` inline - 쇼핑몰 원가 등에 사용되는 취소선(삭제)태그
6. `<address>` block - 회사 주소
7. `&copy;` 특수문자태그 - copyright 약자
## 250806 레이아웃 태그 TIP
* `<div>` : 2개 이상의 블록 또는 인라인을 묶어주는 그룹, 작성과 동시에 반드시 **class 또는 id**를 의미있는 이름으로 작성해야한다.
* `class or id` : 클래스와 아이디 속성은 구분이 필요한 모든 태그에 추가 작성 가능하다. **태그가 2개 이상 연속적으로 작성되어 구분이 필요한 경우** 클래스를 주로 사용.
* `<div id="">` : id는 **반복되지 않는 고유한 이름**을 설정하고 바깥쪽 큰 레이아웃에 주로 사용한다.
* `<div class="">` : class는 **반복될 수 있는 이름**을 설정하고 바깥쪽부터 안쪽까지 다양한 레이아웃에 사용한다.
* `<span></span>` : 2개 이상의 인라인 요소를 묶어주는 그룹 또는 **디자인 구분을 위해 태그를 나눠야할때 형제가 인라인 요소일 경우** 의미가 없는 부분에 자주 이용한다.
### 바로가기링크 준비
* 준비 대상) 클릭할 a 요소와 이동할 위치 요소
1. 이동할 위치에 중복되지 않는 명칭으로 아이디 설정
* `<태그 id="riview_pst"></태그>`
2. 위치로 이동하는 클릭 요소에 위 1번 아이디를 이용한 링크 설정
* `<a href="#review_pst">클릭글자 또는 이미지</a>`
* `#이름` == 임시링크(X) 아이디(O)
* `#` == 임시링크(O) 아이디(X)
### 바로가기 링크 다양한 사용 예
* 같은 페이지의 다른 위치로 이동 시
*`<a href="위치아이디명">클릭요소</a>`
* 다른 페이지의 특정 위치로 이동 시
*`<a href="./상대경로#위치아이디명">클릭요소</a>`
*`<a href="./login.html#search">클릭요소</a>`
## HTML - Form
* 사용자 입력/선택 요소 1개라도 등장 시 전체 영역을 'form'묶어주기 **action, method, id** 필수!
* 폼 내부 양식 종류가 그룹별로 2개 이상 구분될 경우 `fieldset, legend` 작성
* `fieldset` div처럼 그룹 역할이므로 id 또는 class 함께 작성
* `fieldset`을 생략하고 `div, ul, ol, dl` 등 다른 그룹으로 대체 가능
### form - input
* `<input type="종류" name="데이터명" id="데이터명(중복X)" class="공통디자인명">`
* `value`속성은 필요한 경우만 작성. 쇼핑몰 수량 1 기본값 등
# Form 입력과 선택 요소
## `<input type "">`
* type=text : 입력요소/name(데이터구분용)/value(초기값)
* type=checkbox : 선택요소/name(그룹용)/value(데이터구분용)
* 입력 요소 종류 : text, password, mail, search, number 등
* 선택 요소 종류 : checkbox, radio, select, option
* 선택 요소에는 라벨이 필수적으로 따라붙음
* 데이터구분용은 id처럼 해당 데이터만을 구분하는 중복되지 않는 이름을 설정한다.
* 그룹용은 클래스와 같이 2개 이상의 요소를 묶어주는 반복이름개념으로 사용한다.
---
## git 버전관리
### gitHub 폴더 복제 방법
* `git clone 주소 붙여넣기`
### gitHub 수정된 작업물 내려받기
* `git pull origin main`
---
# CSS
## 캐스케이딩 스타일 시트(폭포 단계별로 작성하는 CSS)
### CSS 기초 작성 순서
1. `styles/reset.css` 파일만들기
2. html파일 head 안 `link:css`자동완성 작성하고 위 1번 파일 연결
3. (html 작성 완료 기준) 부모->자식 순서대로 모든 선택자 작성 `{}`중광로 공백
4. 모든 선택자 작성 후 `{속성:값:}`추가 작성하여 디자인 진행하기

## CSS selector
* 선택자`{속성:값;}` / 선택자`{속성:값;속성:값;속성:값;}`
- 선택자 : CSS로 디자인하는 대상
- {} : 속성과 값을 묶어주는 CSS 디자인 괄호
- 속성 : 선택자에 적용하는 속성
- 값 : 속성 값
- ; : 앞 속성값이 여기서 종료했다는 것을 의미

### 색상 속성
1. color : 글자색
2. background-color : 배경색
EX
- `color:rgb(255,255,255);`
- ⭐`color:rgba(255,255,255,0.5);` : a는 투명도
- ⭐`color:#FF00FF;`

### #id
* `<h1 id="heading">제목</h1>`
1. `h1 {color:red;}` - h1만 적용
2. `#heading {color:red;}` - heading 아이디만 적용
3. `h1#heading {color:red;}` - h1의 heading 아이디만 적용

### .class
* `<h1 class="title">제목</h1>`
1. `h1 {color:red;}` - h1만 적용
2. `.title {color:red;}` - title 클래스만 적용
3. `h1.title {color:red;}` - h1의 title 클래스만 적용

### CSS children
* `<div><a></a></div>`
1. `div a { color:red; }` - div내부의 모든 a에 적용
1. `div>a { color:red; }` - div내부 자식 a에만 적용

* `<div class="parents"><a>menu</a></div>`
1. `.parents a {color:red;}` - parents의 모든 a
2. `.parents>a {color:red;}` - parents의 자식 a
3. `div.parents a {color:red;}` - div parents의 모든 a
4. `div.parents>a {color:red;}` - div parents의 자식 a

* `<div class="parents"><a id="nav">menu</a></div>`
1. `.parents #nav {color:red;}` - parents 안의 모든 nav
2. `.parents>#nav {color:red;}` - parents 안의 자식 nav만
3. `div.parents #nav {color:red;}` - div의 class가 parents일때 안의 모든 nav
4. `div.parents>#nav {color:red;}` - div의 class가 parents일때 안의 자식 nav

### CSS sibling
`<div class="parents">`
    `<p>내용1</p>`
    `<h1>제목<h1>`
    `<p>내용2</p>`
    `<p>내용3</p>`
`</div>`
1. `.parent p{color:red;}` - 내용1,2,3
2. `.parent h1+p{color:pink;}` - 내용2
3. `.parent h1~p{color:yellow;}` - 내용2,3

## 스타일조정
### 크기조정
* width와 height로 조정
* 0이 아닌 수에는 단위를 필수로 기입
* ex : `width:400px;` `height:100vh;`(=viewport height) 
### 안쪽여백조정
* 안쪽 여백은 padding으로 조정 (padding-left/right/bottom/top)
* ex : `padding-left:15px;` `padding-right:15px;`
### 바깥여백조정
* 바깥 여백은 margin으로 조정 (margin-left/right/bottom/rop)
* ex : `margin-bottom:16px` 요소끼리 여백만들기 등

*////inline은 여백 안먹힘! block으로 변환해야 먹힌다!////

### 구분선
* `border(-bottom/top) : (사이즈) (실선여부) (색);`
* 테두리와 해당 요소의 거리를 둘 땐 margin이 아닌 padding
* `border-radius:(px);` 모서리 기울기 조절
### 글자정렬
* `text-align:;`
### 
* `overflow:hidden;`
* 자식요소가 부모를 넘어도 부모 범위 이상으로 노출되지 않음

# CSS 글자 속성
## font-family
* `font-family:대표글꼴, 후보글꼴, 글꼴유형`
* 글꼴유형 : snas-serif, serif
* 글꼴명에 한글, 특수문자, 공백이 있을 경우 ``따옴표 묶기
* 윈도우 기본 설치 글꼴 : 굴림, 고딕, 바탕, 궁서
* 대표글꼴이 설치가 필요한 글꼴일 경우 : 해당 글꼴 파일을 웹주소로 연결해서 누구나 볼 수 있게 설정.
<!--프리텐다드(v1.3.9) 웹글꼴 연결주소-->
<link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard-dynamic-subset.min.css" /> 

## font-size
* `font-size:값확장자;`
* 16px 평균값 기준으로 피그마, 포토샵 등에서 디자인한 글자 크기를 `rem, em`단위로 변환하여 작성
* 16px == 1em or 1rem
* rem은 부모크기에 비례하지 않은 본인의 고유 설정값으로 출력됨
* `https://validator.w3.org/nu/#file` 변환사이트

* `font-weigbt:;` 글자굵기 / regular 400 기준 +-100
* `line-height:;` 행간
---
## 수열선택자
* CSS에서 요소를 규칙적으로 선택할때 사용하는 선택자
* `nth-child(n)`형태로 작성, 자식이 2개 이상 있을 때 n번째 자식이라는 개념
* class 와 id로 이름짓기 적합하지 않은 경우에도 css선택이 가능해 다양하게 사용됨

### CSS Margin a padding 방법
* `1px 2px 3px px` : 위->오른쪽->아래->왼쪽
* `1px` : 상하좌우값동일
* `1px 2px` : 상하1 좌우2
* `1px 0 2px` : 상1 좌우0 하2
* margin 겹침현상 주의!
### a inlin 태그를 블록화할때
* `display:block` 또는 `dispaly:inline-block`
### 백그라운드 배경이미지 삽입
* `background-imgh:url(경로);`
* `background-repeat:반복설정;`
* repeat
* no-repeat
* repeat-x
* repeat-y
* `background-position:(방향);`
* x y 순으로 작성
* 값(0%~100%, px, auto) 사용
* `background-size:(이미지크기);`
* 이미지 크기는 `(가로) (세로')` 한 쪽은 auto로 만들어야 비율이 맞는다
* `contaion` - 요소 안에 배경 이미지가 전부 나타나도록 가로세로 조정
* `cover` - 이미지로 요소의 크기를 모두 덮어 씌우는 형태로 적용(이미지잘림)
* 백그라운드 통합
* `background:배경색 주소 반복 포지션 / 크기;`