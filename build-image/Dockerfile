FROM ghcr.io/taha2samy/java:21.0.10_7-LTS-jdk_standard

USER root
RUN usermod -u 1000 java && groupmod -g 1000 java || true

ENV CNB_USER_ID=1001
ENV CNB_GROUP_ID=1001
LABEL io.buildpacks.stack.id="io.buildpacks.stacks.jammy"

RUN chmod -R 755 /opt/java

USER 1001