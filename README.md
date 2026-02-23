# LaTeX env

vscode로 LaTeX 작업을 위해 세팅한 환경.

## How to use

### 리눅스 로컬

1. .devcontainer/Dockerfile 안에 있는 명령어들을 알아서 리눅스에 입력해 직접 설치한다.
2. vscode의 익스텐션으로 latex workshop을 설치한다.
3. vscode로 이 환경을 열어 사용한다.
4. .devcontainer 디렉토리는 지워도 된다.

### 윈도우 로컬

1. texlive를 설치한다.
2. vscode의 익스텐션으로 latex workshop을 설치한다.
3. vscode로 이 환경을 열어 사용한다.
4. .devcontainer 디렉토리는 지워도 된다.

### 맥 로컬

1. 맥 안써봐서 모름

### docker(docker desktop)

1. 리눅스 환경(WSL 가능)에서 docker를 설치하여 사용하는 것을 권장. docker를 설치할 때는 터미널에 다음과 같이 입력하면 된다. (Docker desktop 설치는 비추.)
   ```bash
   curl -fsSL https://get.docker.com -o get-docker.sh
   sudo sh get-docker.sh
   ```
   뭐라 하면서 뜸을 들인 후에 설치해서 시간이 좀 걸리지만 1분 내에 끝난다.  
   [출처 링크](https://docs.docker.com/engine/install/ubuntu/#install-using-the-convenience-script)
2. vscode 내에서 Dev Containers 확장을 설치한다.  
   `Ctrl + shift + X` 를 누르고 검색창에 Dev Containers를 검색하면 나온다.
3. 이 환경을 vscode로 연다.
4. `Ctrl + shift + P` 를 누르고 `Rebuild and Reopen in Container` 검색 후 `Enter`
5. .tex 파일과 .bib 파일을 \ws 안에 만들고 사용하면 된다. 컴파일 결과는 `out` 디렉토리에 생성된다.

## 기능들

1. `ctrl+s` 누를 시 자동 포멧팅
2. 오탈자 지적(익스텐션: code spell checker)
3. LaTeX Workshop의 여러 기능들..
   1. 자동 컴파일 지원
   2. 수식 미리보기 지원
      등등..
