FROM frolvlad/alpine-java:jre8-slim

LABEL maintainer "Serranos Miser <twitter.com/serranos>"

ENV PLANTUML_VERSION=1.2020.7

RUN \
  apk add --no-cache graphviz wget ca-certificates && \
  wget "https://downloads.sourceforge.net/project/plantuml/${PLANTUML_VERSION}/plantuml.${PLANTUML_VERSION}.jar" -O plantuml.jar && \
  apk del wget ca-certificates

ENV LANG en_US.UTF-8

ENTRYPOINT ["java", "-Djava.awt.headless=true", "-jar", "plantuml.jar", "-p"]

CMD ["-tsvg"]
