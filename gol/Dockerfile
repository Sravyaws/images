FROM tomcat:9.0
LABEL user="sravya"
LABEL org="SS"
RUN apt-get update && \
    apt-get install -y openjdk-8-jdk
COPY gameoflife.war **/webapps/gameoflife.war
EXPOSE 8080
CMD ["catalina.sh", "run"]





``` Dockerfile

FROM tomcat:9-openjdk8
ADD <http url> /usr/local/tomcat/webapps/gameoflife.war
EXPOSE 8080


