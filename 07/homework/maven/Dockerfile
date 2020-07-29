FROM ubuntu:18.04
RUN apt-get update \
    && apt-get install -y default-jdk git maven \
    && rm -rf /var/cache/apt
WORKDIR /home
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello
RUN mvn package -f boxfuse-sample-java-war-hello/pom.xml \
    && find boxfuse-sample-java-war-hello/target -type f,d ! -name '*.war' | xargs rm -rf
