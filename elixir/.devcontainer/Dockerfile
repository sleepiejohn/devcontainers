FROM hexpm/elixir:1.11.3-erlang-23.2.2-alpine-3.12.1

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# install common dependencies
RUN apk update
RUN apk add --no-cache \
        git \
        openssh-client \
        gnupg \
        procps \
        lsof \
        htop \
        net-tools \
        psmisc \
        curl \
        wget \
        rsync \
        ca-certificates \
        unzip \
        zip \
        nano \
        vim \
        less \
        jq \
        libgcc \
        libstdc++ \
        krb5-libs \
        libintl \
        libssl1.1 \
        lttng-ust \
        tzdata \
        userspace-rcu \
        zlib \
        sudo \
        coreutils \
        sed \
        grep \
        which \
        ncdu \
        shadow \
        strace

RUN groupadd --gid $USER_GID $USERNAME
RUN useradd -s /bin/bash --gid $USERNAME -m $USERNAME
USER ${USERNAME}
ENV HOME /home/${USERNAME}