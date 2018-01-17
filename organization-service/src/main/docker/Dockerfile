FROM @docker.image.user@/tmx-jdk:1.0

RUN mkdir -p /usr/local/organizationservice
ADD @project.build.finalName@.jar /usr/local/organizationservice/
ADD run.sh run.sh
RUN chmod +x run.sh
CMD ./run.sh
