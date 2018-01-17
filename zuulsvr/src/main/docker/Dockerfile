FROM @docker.image.user@/tmx-jdk:1.0

RUN mkdir -p /usr/local/zuulservice
ADD @project.build.finalName@.jar /usr/local/zuulservice/
ADD run.sh run.sh
RUN chmod +x run.sh
CMD ./run.sh
