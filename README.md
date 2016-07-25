#### 1. Tomcat 서버를 시작할 때 웹 애플리케이션이 초기화하는 과정을 설명하라.
* 1. ContextLoaderListener.contextInitialized()호출
* 2. jwp.sql (sql) , ConnectionManager의 DB 정보로 DB 초기화
* 3. DispatcherServlet.init()에서 매핑 초기화 --> RequestMapper.initMapping()매핑.

#### 2. Tomcat 서버를 시작한 후 http://localhost:8080으로 접근시 호출 순서 및 흐름을 설명하라.
* 1. RequestMapping.initMapping() --> mappings.put("/", new HomeController());
* 2. HomeController.execute()에서는 index.jsp의 JspView와 questionDao 모델을 ModelAndView형태로 리턴.
  
#### 7. next.web.qna package의 ShowController는 멀티 쓰레드 상황에서 문제가 발생하는 이유에 대해 설명하라.
* 
