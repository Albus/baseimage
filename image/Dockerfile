FROM ubuntu:xenial

COPY . /bd_build

RUN /bd_build/prepare.sh \
 && /bd_build/system_services.sh \
 && /bd_build/utilities.sh \
 && /bd_build/cleanup.sh \
 && rm -f /etc/service/sshd/down

ENV DEBIAN_FRONTEND="teletype" \
    LANG="ru_RU.UTF-8" \
    LANGUAGE="ru_RU:en" \
    LC_ALL="ru_RU.UTF-8" \
    TZ="Europe/Moscow"

CMD ["/sbin/my_init"]