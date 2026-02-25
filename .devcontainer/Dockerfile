# Base image
FROM ubuntu:22.04

# installing texlive and utils
RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    texlive-full \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# latexindent의 의존성 패키지들
RUN apt-get update && apt-get install -y --no-install-recommends \
    libyaml-tiny-perl \
    libfile-homedir-perl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# 글꼴 추가
RUN apt-get update && apt-get install -y --no-install-recommends \
    fonts-nanum \
    fonts-noto-cjk \
    fonts-baekmuk \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

ARG USERNAME=latex-user
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m -s /bin/bash $USERNAME \
    && apt-get update \
    && apt-get install -y sudo \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# 3. 마지막에 사용자 전환
USER $USERNAME