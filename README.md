Here we 3 sample projects for spring-boot: http://spring.io/guides/gs/spring-boot/
This solves a problem with application which should work with Tomcat, but you are following tutorial 
http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto-use-jetty-instead-of-tomcat
it doesn't work and ... if you are "old-fashioned" java/spring (like me :) web developer - and you have no idea why it doesn't work, the solution you can find here :)

Somebody "smart" in the tutorial haven't mentioned that if you want to convert a JAR file (fat JAR, whatever) to the WAR file which you can use after in the Tomcat/Jetty
 you have to extends: SpringBootServletInitializer
Adding dependency to jetty/tomat in the pom.xml and changing a packaging is not enough here.

---------------------------------------------------------------
So, solution you can find here:

* gs-spring-boot-init - is a init project, copy of the https://github.com/spring-guides/gs-spring-boot.git

* gs-spring-boot-jetty - works with Jetty container, you have war file war file to the jetty directory e.g. jetty-distribution-9.2.11.v20150529\webapps\
and then open a browser with: http://localhost:8080/gs-spring-boot-0.1.0/

* gs-spring-boot-tomcat - works with Tomcat container, you have to copy war file to the tomcat directory e.g.  apache-tomcat-8.0.23\webapps\
and then open a browser with: http://localhost:8080/gs-spring-boot-0.1.0/



----------------------------------------------------------------
REST example:
http://localhost:8080/gs-rest-service-0.1.0/greeting?name=Daniels