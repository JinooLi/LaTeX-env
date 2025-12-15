# Base image
FROM ubuntu:22.04

# installing texlive and utils
RUN apt-get update && apt-get install -y --no-install-recommends \
    # git은 써야지..??
    git \
    texlive-full \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*


RUN apt-get update && apt-get install -y --no-install-recommends \
    # latexindent의 의존성 패키지들
    libyaml-tiny-perl \
    libfile-homedir-perl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*