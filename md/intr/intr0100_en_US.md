Natural-JS
===

<ul class="contents links" style="width: 218px;margin-left: -233px;top: 157px;"></ul>

## 개요

Natural-JS 는 Natural-CORE, Natural-ARCHITECTURE, Natural-DATA, Natural-UI 로 구성 됩니다. Natural-CORE는 프레임워크에서 내부적으로 사용하는 CORE 라이브러리 패키지이고 Natural-ARCHITECTURE는 복잡한 웹 UI 환경을 구조화, 단순화 시켜주는 CVC Architecture Pattern 기반의 Architecture Framework를 제공 합니다. Natural-DATA는 Data 처리 및 데이터 동기화에 대한 모듈들을 제공 하며 Natural-UI 는 HTML 기반의 Grid, Form, Popup등 여러 가지 컴포넌트를 제공하여 웹 사용자경험과 개발생산성을 증대 시켜 줍니다.

## 개발배경 및 목적

1990년대 등장한 웹 기술은 네트워크의 보급 확산과 정보공유 및 어플리케이션개발의 편의성에 힘입어 폭발적인 성장을 거듭하였습니다. 오늘날 웹 어플리케이션은 개인적 정보 공유로부터 기업의 자원 관리 및 전자정부에 이르기까지 현대인의 생활 전반에 매우 깊이 자리 잡고 있는 필수적인 부분이 되었습니다. 사용자에게 있어 이와 같은 웹 어플리케이션의 모든 기능은 사용자 인터페이스를 통해 보여 집니다. 이러한 사용자 인터페이스는 웹의 종단 사용자들이 경험하는 대화형 워크플로우의 모든 부분에 연관되며, 개발과정에서 가장 많은 시간과 노력이 요구되는 영역입니다. 한 통계자료에 따르면, 웹 어플리케이션 시스템 개발에 있어서 전체 개발 비용 중 유지보수에 관계된 비용은 80%가 사용자 인터페이스와 관련(이성혜, 마이크로소프트웨어, 7월 2003년)이 있다고 합니다. Ajax (Asynchronous Java Script and XML)는 클라이언트 영역에 사용되는 일련의 웹 개발 방법들을 지칭하는 용어로 이러한 사용자 인터페이스 개발을 위한 대표적 기술 중 하나입니다. Ajax를 통하여, 웹 어플리케이션들은 현재 페이지의 디스플레이나 동작에 방해받지 않고 비동기 방식으로 서버로부터 데이터를 검색하고 추출하는 것이 가능합니다. Ajax 기술은 웹 사이트의 능률적이고 역동적인 사용자 인터페이스 개발을 위해 폭넓게 채택되고 있으며, e-mail 시스템, 메시지 링킹, 주식거래 및 전자정부 시스템 등의 다양한 웹 어플리케이션에 향상된 사용자 경험을 제공하기 위해 사용되고 있습니다. 또한 Google이나 facebook등의 초대형 글로벌사이트들은 사용자 편의성을 위해 Ajax기술을 채택하고 있어 Ajax의 중요성을 증명하고 있습니다.

![](images/refr/pic1.png)

<center>[그림1] WEB 2.0을 구현하는 기술</center>

Ajax 기반 클라이언트는 이와 같은 다양한 웹 어플리케이션에서 고급 사용자 경험의 제공을 가능하게 하는 장점이 있지만, 방대한 분량의 코드로 이루어진 복잡한 클라이언트 개발에 있어 웹-개발의 편의성과 유지보수성 등이 낮아지는 단점이 있습니다. 다음은 Ajax기반의 웹 어플리케이션 개발의 대표적인 문제점을 나타내는 그림입니다.

![](images/refr/pic2.png)

<center>[그림2] 현행 Ajax기반의 웹 어플리케이션 개발의 문제점</center>

위와 같은 문제점들을 해결하여 웹-개발의 편의성과 유지보수성 향상을 제공할 수 있는 기술로 MVC (Model-View-Controller) 패턴을 들 수 있는데, 이 패턴은 응용 로직을 사용자 인터페이스와 분리함으로써 구조적 디자인 복잡도를 감소시키고 이를 통해 유지보수성 향상을 제공합니다. MVC 모델은 Smalltalk80의 사용자 인터페이스 디자인에서 발전된 기술로, 다양한 웹 어플리케이션 개발에 보편적으로 적용되는 기술입니다. 하지만, 복잡한 사용자 인터페이스 코드 영역을 일반적인 서버-클라이언트 기반의 MVC 모델에서는 단순히 View 영역으로 구분함으로써 UI의 개발 편의성과 유지보수성을 개선하는데 제한적일 뿐 아니라 비대해지고 다이나믹해진 UI영역의 개발을 수용하기에도 무리가 따릅니다. 이와같이 복잡한 Ajax 기반 클라이언트 개발에 있어, 그 개발편의성을 증대시키고 방대한 코드의 유지보수성을 개선하기 위해, Naturl-JS 를 개발하게 되었습니다. Natural-JS 는 MVC 아키텍처 패턴을 웹 환경에 맞게 개량시킨 CVC(Communicator-View-Controller) 아키텍처 패턴(김황만, 김용구, 한국통신학회, 9월 2011년) 과 이 패턴 기반의 아키텍처 프레임워크를 제공하여 [그림2]와 같은 Ajax 기반 웹 어플리케이션 개발의 여러 가지 문제점들을 해결하고 엔터프라이즈 웹 어플리케이션에서 모바일 웹 어플리케이션까지, 웹 개발 전체의 개발 생산성과 사용자 경험을 월등하게 개선 시켜줄 수 있는 CVC 아키텍처 패턴기반의 프레임워크와 UI 컴포넌트를 제공 합니다.

## 아키텍처 구성

Natural-JS 는 크게 Natural-CORE, Natural-ARCHITECTURE 와 Natural-DATA, Natural-UI 로 나눠집니다. Natural-CORE는 프레임워크에서 전반적으로 사용되어 지는 라이브러리의 패키지이고 Natural-ARCHITECTURE는 웹 어플리케이션 UI 개발에 대한 아키텍처를 제공 해 주고 Natural-DATA는 Data 처리 및 데이터 동기화에 대한 모듈들을 제공 하며 Natural-UI 는 HTML 기반의 Grid, Form, Popup등 여러 가지 컴포넌트를 제공 합니다.

![](images/refr/pic3.png)

<center>[그림3] Natural-JS 아키텍처 구성</center>

### 가. Natural-CORE

![](images/core.png)

Natural-CORE 는 Natural-JS 에서 전역으로 사용하는 공통 라이브러리 패키지입니다. Natural-Core는 다음과 같은 클래스들로 구 되어 있습니다.

*   jQuery 플러그인 확장 : Natural-JS 의 공통 함수를 jQuery 플러그인 형태로 제공하는 라이브러리
*   N : 코어 유틸리티 집합 클래스
*   N.gc : Natural-JS 내부 Garbage Collection 관련 유틸리티 집합 클래
*   N.string : 문자열 조작 관련 함수 집합 클래스
*   N.element : HTML 요소 제어에 관련된 함수 집합 클래스
*   N.date : 날짜 관련 함수 집합 클래스
*   N.browser : 웹 브라우저와 관련 된 함수 집합 클래스
*   N.message : 메시지 처리 관련 함수 집합 클래스, 메시지 리소스의 데이터 처리 및 다국어 처리등의 역할을 수행
*   N.array : Array 가공에 관련 함수 집합 클래스
*   N.json : JSON 데이터 가공에 관련 함수 집합 클래스
*   N.event : 이벤트 관련 함수 집합 클래스

### 나. Natural-ARCHITECTURE

![](images/architecture.png)

Natural-JS 는 CVC 아키텍처 패턴 기반의 Natural-Architecture Framework 를 제공하여 웹 어플리케이션 UI 개발의 복잡성을 해결하고 개발생산성을 향상 시켜줍니다. Natural-ARCHITECTURE 는 다음 다이어그램과 같이 구성되어 있습니다.

![](images/refr/pic4.png)

<center>[그림4] Natural-ARCHITECTURE</center>

#### 1) CVC Architecture Pattern

CVC 아키텍처 패턴은 기존 MVC로 구현된 서버중심 웹 어플리케이션에서 단순 뷰(View) 영역을 표현하던 클라이언트 브라우저를 [그림5]와 같이 클라이언트중심의 MVC로 구성하고 서버를 데이터만 서비스해주는 단순 Model 영역으로 정의하여 MVC를 바라보는 관점을 서버중심에서 클라이언트 중심으로 이동 하는것이 CVC아키텍처 패턴의 핵심이론입니다. 이로서 클라이언트 브라우저를 웹 어플리케이션 서버와 서버기술의 종속성으로부터 탈피시킬 수 있고 디자인영역과 개발영역을 완벽하게 분리하여 개발의 복잡도를 낮출 수 있습니다.

![](images/refr/pic5.png)

<center>[그림5] CVC Architecture Pattern</center>

#### 2) Natural Architecture Framework

Natural Architecture Framework 는 CVC Architecture Pattern 의 Communicator 영역이 N.comm 클래스로 구현 되어 있고, Controller 영역은 N.cont 클래스로 구현되어 있습니다. View 는 이를 구현한 구현체는 존재하지 않고 개발 스크립트가 첨부 되어있지 않는 순수 HTML 영역이 view 요소로 정의 되어 있습니다. N.comm 은 서버에 JSON 형태의 데이터를 송신/수신 하고 블록 페이지들을 불러오는 역할을 담당 합니다. 또한 블록 페이지 간 전송 되는 데이터와 요청 정보들을 확인 할 수 있는 N.comm.request 객체를 제공 하고 N.comm 으로 통신하는 모든 요청과 응답 사이에 공통 실행 로직 이나 공통 데이터 처리기를 적용 할 수 있는 Communication Filter 기능을 제공 합니다. N.cont 는 View 의 DOM 을 컨트롤 하거나 요소에 이벤트를 바인드 하고 데이터를 바인드를 하거나 View 로 부터 데이터를 가져와 Communicator 에 전달 해 주는 역할을 수행 합니다. 또한 Controller 객체의 사용자 정의 메서드들에 대해서 AOP(Aspect-Oriented Programming) 를 적용 할 수 있습니다. View 는 개발 스크립트가 첨부되지 않은 순수 HTML만으로 View를 구현 할 수 있는 방법을 Natural-ARCHITECTURE 에서 가이드 하고 있습니다.

![](images/refr/pic6.png)

<center>[그림6] Natural Architecture Framework</center>

Natural Application Context(N.context)는 Natural-JS 의 생명주기(Life-Cycle) 안의 데이터 저장소 역할을 수행 하며 설정 데이터, 메시지 리소스 등을 저장 하고 관리할 수 있는 기능을 제공 합니다.

### 다. Natural-DATA

![](images/data.png)

Natural-DATA 는 서버에서 가져온 데이터나 직접 작성한 JSON 데이터를 가공(정제, 조작)할 수 있는 기능과 데이터를 양식화(Format), 검증(Validate)을 할 수 있는 기능과 동일한 데이터를 사용하는 컴포넌트나 라이브러리 간 실시간으로 데이터를 동기화 해 주는 기능을 제공 합니다. Natural-JS 는 데이터와 데이터가 표현될 HTML 요소(Element)의 값이 분리되어 있습니다. 원(元) 데이터는 메모리에 저장되고 HTML 요소에 표시되는 값 들은 단지 보여주는 값들로만 처리 됩니다(입력요소에 의한 입력 값 들은 제외). HTML 입력 요소들(input, select, textarea 등)을 통해서 입력 값이 수정되거나 생성되면 이와 연결되어 있는 메모리의 데이터도 자동으로 수정/생성 됩니다. 때문에 서버와의 데이터 송신/수신 시 메모리의 원 데이터만 참고하면 되어서 개발이 간편 해 집니다. 다음은 Natural-DATA 패키지의 라이브러리들에 대한 설명입니다.

#### 1) DataSync

DataSync는 동일한 데이터를 사용하는 컴포넌트나 라이브러리간 데이터 동기화를 보장 해주는 Data Observer 역할을 수행하는 라이브러 입니다.

#### 2) Formatter

Formatter는 주어진 데이터를 양식화된 데이터로 변환하거나 HTML 입력요소에 양식화된 데이터를 표시 해 줍니다. 제공되는 이벤트들을 활용하면 입력요소(Input Element)에 사용자가 입력한 값에 대한 실시간 Formatting 기능도 간단하게 구현 할 수 있습니다. 또한 유용한 Formatting Rule 들이 기본으로 탑재 되어 있어 있습니다. 물론 사용자 정의 Rule 들도 손쉽게 추가 할 수 있습니다.

#### 3) Validator

Validator는 주어진 데이터나 HTML 입력요소의 값을 검증하여 결과 데이터를 반환하거나 HTML 입력요소에 메시지를 표시 해 줍니다. 또한 유용한 Validation Rule 들이 기본으로 탑재 되어 있습니다. 물론 사용자 정의 Rule 들도 손쉽게 추가 할 수 있습니다.

#### 4) Utilities

Natural-JS는 JSON 객체 배열 조작의 편의성을 제공하기 위해서 다음과 같 유틸리티를 제공합니다.

*   N.data.refine : 서버에서 가져온 데이터를 Natural-JS UI 컴포넌트에서 사용 할 수 있도록 데이터를 정제
*   N.data.filter : 조건에 의한 JSON 객체 배열 데이터의 컬럼 별 필터링
*   N.data.sort : JSON 객체 배열 데이터의 컬럼 별 정렬

### 라. Natural-UI

![](images/ui.png)

Natural-JS 는 표준 웹 기반의 RIA(Rich Internet Application)를 손쉽게 구현 하기 위한 다양한 컴포넌트를 제공 합니다. 모든 컴포넌트는 개개별로 사용할수도 있지만 결합되어 사용되어질 경우 모두 유기적으로 연동되어 좀더 편리하고 강력한 개발 환경을 제공 해 줍니다. 또한 컴포넌트들에 대한 기본 옵션을 Global Config 에 지정할 수 있어 통일된 UI 환경을 손쉽게 구성 할 수 있습니다. 물론 컴포넌트 생성 시 컴포넌트 옵션을 따로 지정 할 수 있습니다. Data 와 관련된 컴포넌트들(Select, Form, List, Grid, Pagination, Tree)은 실제 데이터(메모리에 저장)와 HTML 요소로 보여지는 데이터가 따로 관리 되어 집니다. Grid를 예를 들면 화면에서 새로운 행을 생성하면 메모리의 데이터도 새로운 행이 생성되고 값을 수정하면 메모리의 값도 실시간으로 수정됩니다. Formatter, Validator 등 Data 조작과 검증에 관련된 라이브러리들도 이 메모리의 데이터를 기반으로 동작 됩니다. 수정, 입력, 삭제 된 데이터를 서버로 보낼때는 화면의 입력요소들 마 가져올 필요 없이 자동으로 동기화되어진 메모리의 데이터만 보내면 되어서 컴포넌트의 데이터를 DBMS의 데이와 손쉽게 동기화 할 수 있습니다. 또한 UI 컴포넌트들은 Controller 영역에서 컴포넌트의 기본 옵션을 직접 적용할 수 있는 명령형 옵션과 컴포넌트의 기본옵션과 서브옵션을 view 영역의 HTML 요소의 data 속성에 JSON 타입의 문자열로 지정할 수 있는 선언형 옵션을 지원합니다(선언형 옵션과 명령형 옵션의 지원 항목은 컴포넌트 기능의 속성에 따라 일치 하지 않을 수 있습니다).

Natural-UI는 다음과 같은 컴포넌트들과 구조로 구성 되어 있습니다.

![](images/refr/pic7.png)

<center>[그림7] Natural-UI</center>

#### 1) Alert(N.alert)

Alert 은 Javascript 의 window.alert 이나 window.confirm 같은 메시지를 표현을 위한 컴포넌트입니다. N.alert은 메시지 다이얼로그를 모달 레이어나 일반 레이어 타입으로 표시 해 줍니다.

#### 2) Button(N.button)

Button 은 HTML a, button, input중 타입이 button인 요소들을 기본버튼모양으로 만들어 줍니다. 명령형으로 옵션을 지정할 수 있지만 편의성을 위해 선언형 옵션으로 버튼 요소의 data-opts 속성(attribute)에 옵션으로 넓이, 기본크기, 색상, 비활성화 여부를 지정 할 수 있습니다. Button 은 유일하게 여러 버튼요소를 한번에 초기화 할 수 있습니다.

#### 3) Datepicker(N.datepicker)

Datepicker 는 날짜를 선택 하여 입력 할 수 있는 컴포넌트입니다. 날짜 포맷은 전역(Config)으로 설정한 포맷을 따르며 Grid나 Form 에 연계되어 사용되어질 경우 Format 룰의 세 번째 인자로 date(Datepicker) 나 month(Monthpicker)를 지정하면 Grid와 Form 에 자동으로 연동되어 표시되며 선택한 값이 메모리의 데이터에 실시간 반영 됩니다.

#### 4) Popup(N.popup)

Popup 은 레이어 팝업을 손쉽게 구현할 수 있는 컴포넌트 입니다. 레이아웃을 표현할 수 있는 특정 요소(DIV, SPAN TABLE 등의 BLOCK 요소)를 팝업으로 만들 수 있고 특정페이지를 가져와 팝업으로 만들 수도 있습니다. 또한 Grid, Form과 연동하여 사용하면 Grid와 상세조회 팝업이 연동된 페이지를 쉽게 만들 수 있습니다.

#### 5) Tab(N.tab)

Tab 은 여러 컨텐츠 패널을 하나의 콘텐츠 영역으로 표현해 주는 컴포넌트입니다.

#### 6) Select(N.select)

Select 는 select, input 태그의 type이 radio, checkbox인 선택 입력 요소들에 데이터 리스트를 바인드(Bind)하여 선택요소의 선택항목들을 자동으로 구현해주는 컴포넌트 입니다. 데이터를 바인딩 하는 기능 외에 값을 가져올 때 선택된 값만 가져오는 것이 아니라 선택한 값이 포함된 row data set 을 가져올 수 있는 기능도 제공 해 줍니다.

#### 7) Form(N.form)

Form 은 리스트 데이터(array[json object])의 특정 로우(Row) Data를 HTML 요소에 값을 바인드(Bind) 해 주는 컴포넌트입니다. 그리드와 연계된 상세화면 보기나 그리드의 조회조건에 해당하는 입력요소의 값을 손쉽게 컨트롤 하는데 사용됩니다. 또한 신규 입력페이지 등 에서도 손쉽게 입력요소를 기반으로 데이터를 생성하고 입력 데이터 및 표현 데이터에 대한 실시간 양식화(Formatting)와 검증(Validate)할 수 있는 기능을 제공합니다. 데이터 레이아웃을 표현하는 HTML 요소(DIV, SPAN, TABLE등)를 지정하면 지정한 요소의 하위요소(Children Elements)중에서 Data의 컬럼명과 일치하는 식별자(태그의 id 속성)를 가진 요소를 찾아 값을 바인드 해 주어 데이터 폼을 쉽게 구현 해 줍니다.

#### 8) List(N.list)

List 는 메모리에 저장되어 있는 리스트 데이터(array[json object])를 HTML UL/LI 태그 기반의 리스트로 표현 해 줍니다. List 컴포넌트는 미리 정의한 HTML UL/LI 요소를 그대로 그리드 컴포넌트화 해줍니다. 때문에 컴포넌트 디자인에 대한 제약이 전혀 없어 퍼블리싱된 HTML UL/LI 요소에 List 컴포넌트만 실행시켜주면 아주 손쉽게 데이터 목록 화면을 완성 할 수 있습니다. 스크롤 페이징, 행(row)의 추가·삭제등의 기능과 표시 데이터와 입력 데이터에 대한 실시간 양식화(Formatting), 검증(Validate) 기능을 제공 해 줍니다. 또한 리스트의 각 행의 요소 및 데이터를 제어를 하기위한(RowHandler) 기능을 제공 함으로서 리스트 조작에 대한 한계를 극복할 수 있습니다.

#### 9) Grid(N.grid)

Grid 는 메모리에 저장되어 있는 리스트 데이터(array[json object])를 HTML TABLE 태그 기반의 데이타 그리드로 표현 해 줍니다. 다른 그리드 컴포넌트들과 달리 미리 정의한 HTML TABLE 요소를 그대로 그리드 컴포넌트화 해줍니다. 때문에 그리드 디자인에 대한 제약이 전혀 없어 퍼블리싱된 HTML TABLE 요소에 Grid 컴포넌트만 실행시켜주면 아주 손쉽게 데이터 그리드를 완성 할 수 있습니다. 컬럼 리사이징, 스크롤 페이징, 행(row)의 추가·삭제, 컬럼정렬(Sort)등 일반적인 데이터그리드의 기능 외에 표시 데이터와 입력 데이터에 대한 실시간 양식화(Formatting)와, 검증(Validate) 기능을 제공 해 줍니다. 또한 그리드의 각 행의 요소 및 데이터를 제어를 하기위한(RowHandler) 기능을 제공 함으로서 그리드 조작에 대한 한계를 극복할 수 있습니다.

#### 10) Pagination(N.pagination)

Pagination 은 데이터 표현에 대한 브라우저의 부하를 줄이기 위해 데이터를 지정한 갯수만큼 잘라서 보여주는 컴포넌트입니다. N.grid 와 연동하여 사용하면 서버단 페이징(DB 쿼리 페이징) 및 브라우저 단 페이징(전체 조회 후 잘라서 보여주기) 을 쉽게 구현 할 수 있습니다. 또한 페이징이 필요한 어떠한 목록도 페이징 처리를 할 수 있습니다.

#### 11) Tree(N.tree)

Tree 는 계층 구조의 데이터를 트리 타입으로 표현 해 주는 컴포넌트입니다.

### 마. Natural-UI.Shell

Natural-UI 가 컨텐츠 영역의 UI 개발을 지원 한다면 Natural-UI.Shell 은 컨텐츠영역 바깥의 쉘(Shell) 영역의 개발을 지원 하는 컴포넌트 패키지 입니다.

Natural-UI.Shell은 다음과 같은 컴포넌트들로 구성 되어 있습니다.

#### 1) Notify(N.notify)

Notify 는 사이트 전역 알림 메시지를 표시하는 컴포넌트 입니다.

Alert(N.alert)는 컨텐츠 영역의 메시지를 처리하는 용도이고 N.notify는 사이트 전역의 메시지를 처리 하는 용도 입니다. 때문에 N.alert의 요소(Element)는 주로 document.body.[pageContext] 영역에 생성 되고 N.notify는 document.body 영역에 생성 됩니다.

#### 2) Documents(N.docs)

Documents 는 Natural-JS 로 제작 된 메뉴 페이지들을 Multi Document 나 Single Document 타입으로 표시 할 수 있는 페이지 컨테이너 입니다.

## 개발언어

*   Javascript / jQuery 1.12.4
*   HTML4 / HTML5
*   CSS2 / CSS3

## 지원 브라우저

*   PC : Internet Explorer 8 이상(Internet Explorer 9 이상에 최적화 되어 있음), Chrome, Firefox, Safari(OSX), Opera 최신 버전
*   모바일 : iOS Safari, iOS UIWebView, Android Browser, Android Chrome, Android WebView

## 라이센스

*   GNU LGPL(Lesser General Public License) v2.1
*   LGPL은 GPL보다는 훨씬 완화된(lesser) 조건의 공개 소프트웨어 라이센스입니다. 가장 큰 차이점은 LGPL 코드를 정적(static) 또는 동적(dynamic) 라이브러리로 사용한 프로그램을 개발하여 판매/배포할 경우에 프로그램의 소스코드를 공개하지 않아도 된다는 점입니다. LGPL 코드를 사용했음을 명시만 하면 됩니다. 단, LGPL 코드를 단순히 이용하는 것이 아니라 이를 수정한 또는 이로부터 파생된 라이브러리를 개발하여 배포하는 경우에는 전체 코드를 공개해야 합니다.

## 교육 및 지원

*   bbalganjjm@gmail.com 으로 문의