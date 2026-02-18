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