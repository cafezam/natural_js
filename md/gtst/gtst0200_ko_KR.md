샘플 프로젝트로 시작하기(작업 중)
===

[eclipse]: https://www.eclipse.org/downloads/eclipse-packages/

[img-0]: ./images/gtst/gtst0200/0.png
[img-1]: ./images/gtst/gtst0200/1.png
[img-2]: ./images/gtst/gtst0200/2.png
[img-3]: ./images/gtst/gtst0200/3.png
[img-4]: ./images/gtst/gtst0200/4.png
[img-5]: ./images/gtst/gtst0200/5.png
[img-6]: ./images/gtst/gtst0200/6.png
[img-7]: ./images/gtst/gtst0200/7.png
[img-8]: ./images/gtst/gtst0200/8.png
[img-9]: ./images/gtst/gtst0200/9.png

## 샘플 프로젝트 구성

샘플 프로젝트의 기술 요소들은 다음과 같이 구성 되어 있습니다.

> * **Front-End**
     * 기반기술 : HTML, CSS, Javascript
     * 프레임워크 : Natural-JS
> * **Back-End**
     * 기반기술 : JAVA
     * 프레임워크 : Spring Boot
     * DB : HSQLDB

## 설치

### 1. 이클립스 설치
[이클립스 사이트][eclipse] 에서 Eclipse IDE for Java EE Developers 를 다운로드 받아 이클립스를 실행 합니다.
실행 후 편한 작업을 위해 Help > `Eclipse Marketplace` 메뉴를 클릭 하고 Find 입력 요소에  `sts` 로 검색 하면
다음 그림과 같이 `Spring Tools` 플러그인이 조회 됩니다. `install` 버튼을 클릭하여 설치 합니다.

![Spring Tools 설치][img-0]

설치가 완료 되면 이클립스를 재 기동 합니다.

### 2. Github 에서 natural-js-spring-boot 프로젝트 내려받기
설치가 완료 되었으면 이클립스에서 다음 순서대로 실행 합니다.

먼저 아래 URL 을 선택 후 복사(Ctrl + C) 합니다.
```md
https://github.com/bbalganjjm/natural_js.git
```

2.1. 좌측 `Package Explorer` 나 `File` 메뉴 에서 `Import` 를 선택 합니다.

![Import 선택][img-1]

2.2. `Import` 다이얼로그 화면에서 `Git > Projets from Git` 을 선택 하고 `Next` 버튼을 클릭 합니다.

![Projets from Git 선택][img-2]

2.3. Clone URI 를 선택 하고 `Next` 버튼을 클릭 합니다.

![img-3][]

2.4. Natural-JS 의 Source Git Repository 접속 정보를 입력 하는 화면 입니다. 처음에 복사 해둔 URL 에 의해 값들이 자동으로 입력 되어 있을 겁니다. 입력이 되어 있지 않으면
```md
https://github.com/bbalganjjm/natural_js.git
```
를 타이핑 합니다.
아래 그림에서 `User` 와 `Password` 는 Git 로그인 정보를 입력 하면 됩니다. 인증 정보를 저장 하려면 `Store in Secure Store` 를 체크하고 `Finish` 버튼을 클릭 합니다.

![img-4][]

2.5. Natural-JS Source Git Repository 의 브랜치 목록에서 natural-js-spring-boot 브랜치 만 체크 한 후 `Finish` 버튼을 클릭 합니다.

![img-5][]

2.6. `Directory` 입력 항목에 받아 올 소스코드를 저장 할 대상 디렉토리를 지정 하고 `Finish` 버튼을 클릭 합니다.

![img-6][]

2.7. `Wizard for project import` 섹션에서 `import as general project` 라디오 버튼을 선택 후 `Finish` 버튼을 클릭 하고 소스코드를 다운로드하여 프로젝트가 생성 될 때 까지 기다 립니다.

![img-7][]

2.8. 프로젝트가 생성되면 생성 된 프로젝트명을 마우스 오른쪽 버튼으로 클릭 한 후 `Configure` > `Convert to Maven Project` 메뉴를 선택하여 Maven Project 로 만들어 줍니다.

![img-8][]

Maven 프로젝트로 전환이 완료 될 때 까지 기다립니다.

2.9. Maven 프로젝트로 전환이 완료 되었으면 프로젝트명을 마우스 오른쪽 버튼으로 클릭 한 후 `Run As` > `Spring Boot App` 메뉴를 선택하여 프로그램을 구동 합니다.

![img-9][]

2.10 프로그램 구동이 완료 되면 웹 브라우저를 열어 다음 주소를 입력 합니다.
```md
http://localhost/index.html
```
현재 보고 있는 Natural-JS 사이트가 정상적으로 표시 되면 설치가 완료 된 것 입니다.

## 예제
Natural-JS 홈페이지의 예제는 서버와 연동되어 있지 않는 클라이언트 소스 예제 이지만 `natural-js-spring-boot` 프로젝트의 예제는 DB 와 연동 되어 CRUD(생성,조회,수정,삭제) 가 물리적으로 처리 되는 예제 입니다.

다음은 예제 소스코드들에 대한 설명 입니다.

#작업 중...