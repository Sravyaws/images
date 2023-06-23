FROM tomcat:9.0
LABEL user="sravya"
LABEL org="SS"
RUN apt-get update && \
    apt-get install -y openjdk-8-jdk
COPY gameoflife.war **/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]