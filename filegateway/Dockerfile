FROM elixir:slim

RUN apt update && \
    apt install -y proftpd openssh-server git binutils wget dos2unix && \
    mkdir -p /home/ftp && \
    chown ftp:nogroup /home/ftp && \
    mkdir /home/ftp/root && \
    chown root:root /home/ftp/root && \
    chmod 600 /home/ftp/root && \
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
    chmod 700 /home/fgtest/.ssh/ && \
    mkdir /s3 && \
    wget https://dl.min.io/server/minio/release/linux-amd64/minio -O /usr/local/bin/minio && \
    wget https://dl.min.io/client/mc/release/linux-amd64/mc -O /usr/local/bin/mc && \
    chmod +x /usr/local/bin/{minio,mc} && \
    mix local.hex --force && \
    mix local.rebar --force