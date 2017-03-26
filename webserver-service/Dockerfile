FROM maprtech/pacc:5.2.0_2.0_ubuntu14

EXPOSE 8080

# Create a directory for your MapR Application and copy the Application
RUN mkdir -p /usr/share/mapr-apps/
COPY ./target/webserver-service-1.0-SNAPSHOT-jar-with-dependencies.jar /usr/share/mapr-apps/webserver-service.jar
COPY run.sh /usr/share/mapr-apps/run.sh
RUN chmod +x /usr/share/mapr-apps/run.sh
RUN apt-get install -y software-properties-common python-software-properties
RUN add-apt-repository ppa:openjdk-r/ppa
RUN apt-get update
RUN apt-get install openjdk-8-jre

 #CMD ["start", "/usr/share/mapr-apps/run.sh", "/apps/sensors:computer" , "/apps/logs/"]
