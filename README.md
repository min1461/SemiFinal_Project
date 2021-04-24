# SemiFinal_Project


## 국비교육 프로젝트 : EAT-iT
### Project Duration and Members
+ Project Duration
    + 2021.02.04 ~ 2021.02.22 참여인원 : 6명
+ Members
    + [강민규](https://github.com/min1461/)
        + 나의 기여도 : GUI(5%), SERVER(15%), DB(55%), 전체(15%) 
    + [김진환](https://github.com/stux12/)
        + 기여도 : GUI(21%), SERVER(30%), DB(15%), 전체(22%)
    + 엄희경
        + 기여도 : GUI(20%), SERVER(20%), DB(15%), 전체(20%)
    + [이해준](https://github.com/dlgowns)
        + 기여도 : GUI(18%), SERVER(10%), DB(5%), 전체(14%)
    + [최유정](https://github.com/sun0326)
        + 기여도 : GUI(13%), SERVER(12.5%), DB(5%), 전체(10%)
    + [함지웅](https://github.com/dbtkaqkf)
        + 기여도 : GUI(23%), SERVER(12.5%), DB(5%), 전체(19%)
        
### Development Environment
+ OS
    + Window 10
+ Development Tool
    + Eclipse, Oracle SQL Developer
+ Language/Skills
    + Java, HTML5, CSS3, JavaScript, JSP, Servlet, JSTL, jQuery
+ Server
    + Apache Tomcat 8.5  
+ DB
    + Oracle DB

### Introduction
+ 원하는 정보를 쉽게 검색, 맛집 정보를 얻을 수 있는 서비스를 제공
+ 상황에 따라 무엇을 먹을지 고민하는 사용자들
+ 사용자들의 후기를 통해 더욱 신뢰성 있는 맛집 정보 제공

### Develop Detail
+ 제안
    + 배달의 민족이나 요기요 등의 애플리케이션을 통해 맛집에 대한 정보를 쉽게 얻을 수 있습니다.
    + 이를 기반으로 하여 웹을 통해 맛집에 대한 정보를 제공하고 사용자들이 맛집에 대한 평가를 남김으로써 리뷰수에 의해 신뢰 있는 맛집을 순서대로 호출할 수 있도록 구성하고자 하였습니다.
    + 서울시 내에 있는 맛집을 기반으로 하여 DB를 구성하고 특정 구에서 영업하고 있는 맛집, 먹고 싶은 음식의 종류에 따른 맛집 등 여러 가지 방법으로 DB를 호출하고 페이지를 호출하고자 하였습니다.
    + 로그인을 통해 리뷰를 남기고, 맛집에 상세 정보를 확인할 때 지도를 웹에 호출하도록 구성하였습니다
+ 기획
    + 메인화면에서 드롭박스, 자동슬라이드 기능 등을 구현
    + 로그인 시 모든 정보를 입력하지 않을 경우, input태그 하단영역에 메세지가 나오도록 구현
    + 찜한 가게들을 DB에 저장하고 찜 리스트에서 해당하는 가게만 호출하도록 구성
    + 결과 페이지에서 DB에 저장되어있는 좌표를 활용하여 지도에 해당 위치를 표시
    + 리뷰작성시 로그인한 회원은 본인이 작성한 리뷰만 삭제할 수 있도록 구성(관리자는 모든 사람의 리뷰를 삭제할 수 있다.)
    + 가게별 이미지의 경로를 DB에 저장하여 각각 img 태그를 활용하여 각각 호출하도록 함
+ DB설계
    + 상호, 지도,이미지,리뷰, 사용자,찜의 테이블을 구성
    + 해당 데이터를 호출하거나, 리뷰추가(INSERT),리뷰삭제(DELETE)를 이용하여 데이터를 저장 및 호출함.
        + [DB_ERD](./presentation/DB/2조_DB_ERD.pdf) - 링크 수정 必 
+ 개발

### GitHub 구조
- presentation : 국비지원 교육과정중 프로젝트 발표를 위해 작성
    - DB
      - 2조_DB_create.sql
      - 2조_DB_ERD.pdf
      - 2조_DB_insert.sql 
    - 발표용_ppt.pdf
    - 프로젝트 개발 계획서
    - 프로젝트 완료 보고서.hwp
    - 프로젝트 완료 보고서.pdf
    - 화면설계서 및 기능설계서.pdf
- src : 작성코드
    - com : Servlet 내용 작성
    - DB_CONN : DB연동을 위한 Connection 작성
    - DB_DAO : Data를 호출하기위한 Quary문 작성
    - DB_VO : 호출할 데이터를 불러오기위한 DTO(VO)
- Webcontent : 화면구현
    - Client : 클라이언트용 화면구현
    - CSS : CSS 구현
    - img : 로고, 간단한 이미지 등
    - mainframe : header.jsp / footer.jsp의 경로
    - Manager : 회원 전체를 불러오기 위한 화면 구현
    - subpage : 카테고리별 화면 
