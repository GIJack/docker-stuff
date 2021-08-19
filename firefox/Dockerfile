FROM archlinux

LABEL maintainer="GI_Jack - <GI_Jack@hackermail.com>"
LABEL description="Firefox in a container"

RUN pacman -Syu --noconfirm firefox

COPY start_firefox.sh "/opt/start_firefox.sh"

RUN export uid=1000 gid=1000 && \
    mkdir -p /home/firefox && \
    echo "firefox:x:${uid}:${gid}:Developer,,,:/home/firefox:/bin/bash" >> /etc/passwd  && \
    echo "firefox:x:${uid}:" >> /etc/group  && \
    echo "firefox ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers  && \
    chmod 0440 /etc/sudoers  && \
    chown ${uid}:${gid} -R /home/firefox

# set up and run firefox
USER firefox
ENV HOME /home/firefox
ENTRYPOINT '/opt/start_firefox.sh'
