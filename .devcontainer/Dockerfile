# Base image
FROM ubuntu:22.04

# installing texlive and utils
RUN apt-get update && apt-get install -y --no-install-recommends \
    # git은 써야지..??
    git \
    # --- 필수 기반 패키지 ---
    texlive-latex-base \
    texlive-latex-recommended \
    latexmk \
    # --- 참고문헌 관리 (biblatex 사용 시 필수) ---
    biber \
    # --- 폰트 관련 ---
    texlive-fonts-recommended \
    # --- 한국어 지원 ---
    texlive-lang-korean \
    # --- 수학 & 과학 ---
    # amsmath, amssymb, amsthm 등 대부분의 수학 기호 및 정리를 포함.
    texlive-science \
    # --- 그림, 그래프, 색상 등 (TikZ, PGFPlots 포함) ---
    # 제어 시스템 블록 다이어그램이나 그래프를 그리는 데 유용함.
    texlive-pictures \
    # --- 추가 유틸리티 (하이퍼링크, 코드 블록 등) ---
    # hyperref, listings, booktabs, geometry 등 유용한 패키지 다수 포함
    texlive-latex-extra \
    # latexindent를 사용하기 위함.
    texlive-extra-utils \
    libyaml-tiny-perl \
    libfile-homedir-perl \
    # --- [추가] 학회 및 출판사 포맷 (IEEEtran 포함) ---
    texlive-publishers \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set the default username
ENV USERNAME="latex"

# Create a user 'latex' and add to sudoers group
RUN useradd -m ${USERNAME} 

# Set default shell of latex user to bash
RUN chsh -s /bin/bash ${USERNAME}

# Switch to latex user
USER ${USERNAME}