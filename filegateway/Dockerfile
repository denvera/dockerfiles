FROM elixir:slim

RUN apt update && \
    apt install -y proftpd openssh-server && \
    mkdir -p /home/ftp && \
    mkdir -p /testshare && \
    chmod 777 /testshare && \
    mkdir -p /var/run/proftpd && \
    mkdir /run/sshd && \
    useradd -m -s /bin/sh fgtest && \
    chown -R fgtest /home/fgtest/ && \
    mkdir /home/fgtest/root/ && \
    chown root:root /home/fgtest/root && \
    chmod 600 /home/fgtest/root && \
    usermod -p fgtest123 fgtest && \
    mkdir -p /home/fgtest/.ssh/ && \
    chmod 600 /home/fgtest/.ssh/ && \
    mix local.hex --force && \
    mix local.rebar --force
