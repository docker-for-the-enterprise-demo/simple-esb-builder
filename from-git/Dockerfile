FROM dockerfile/java:oracle-java7

RUN apt-get update

RUN apt-get install -y maven

RUN cd /tmp \ 
&& git clone https://github.com/docker-for-the-enterprise-demo/simple-esb.git \
&& cd simple-esb \
&& mvn -Dmaven.test.skip=true package \
&& cp target/*.jar /data/ \
&& cp -rf target/lib /data/ \
&& rm -r ~/.m2/repository/

VOLUME /data

CMD ["/bin/true"]

