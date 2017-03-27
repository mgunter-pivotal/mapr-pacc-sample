FROM maprtech/pacc:5.2.0_2.0_ubuntu14

# Create a directory for your MapR Application and copy the Application
RUN mkdir -p /usr/share/mapr-apps/
COPY ./target/sensor-service-1.0-SNAPSHOT-jar-with-dependencies.jar /usr/share/mapr-apps/sensor-service.jar
COPY run.sh /usr/share/mapr-apps/run.sh
RUN chmod +x /usr/share/mapr-apps/run.sh
RUN apt-get install jq

#CMD ["start", "/usr/share/mapr-apps/run.sh", "/apps/sensors:computer"]
CMD ["start", "ping", "localhost"]
