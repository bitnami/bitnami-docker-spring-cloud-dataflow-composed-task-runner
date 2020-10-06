FROM docker.io/bitnami/minideb:buster
LABEL maintainer "Bitnami <containers@bitnami.com>"

ENV HOME="/" \
    OS_ARCH="amd64" \
    OS_FLAVOUR="debian-10" \
    OS_NAME="linux"

COPY prebuildfs /
# Install required system packages and dependencies
RUN install_packages acl ca-certificates curl gzip libc6 libgcc1 procps tar
RUN . /opt/bitnami/scripts/libcomponent.sh && component_unpack "java" "1.8.265-0" --checksum 6c85e8df954fca444f2471195524db015ec24a67e42f43579401f2adb5189cb8
RUN . /opt/bitnami/scripts/libcomponent.sh && component_unpack "spring-cloud-dataflow-composed-task-runner" "2.6.3-0" --checksum 0bc44df1c7eec646de180d93ef0b45975c71f8f1b4f92422b04865abb70ee4f0
RUN . /opt/bitnami/scripts/libcomponent.sh && component_unpack "gosu" "1.12.0-2" --checksum 4d858ac600c38af8de454c27b7f65c0074ec3069880cb16d259a6e40a46bbc50
RUN apt-get update && apt-get upgrade -y && \
    rm -r /var/lib/apt/lists /var/cache/apt/archives
RUN chmod g+rwX /opt/bitnami
RUN mkdir /.m2 && chmod -R g+rwX /.m2

COPY rootfs /
ENV BITNAMI_APP_NAME="spring-cloud-dataflow-composed-task-runner" \
    BITNAMI_IMAGE_VERSION="2.6.3-debian-10-r7" \
    PATH="/opt/bitnami/java/bin:/opt/bitnami/common/bin:$PATH"

USER 1001
ENTRYPOINT [ "/opt/bitnami/scripts/scdf-composed-task-runner/entrypoint.sh" ]
CMD [ "--help" ]