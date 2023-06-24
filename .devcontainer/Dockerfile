FROM debian:bullseye

RUN apt-get update && apt-get install -y \
    wget \
    build-essential \
    libffi-dev \
    libssl-dev \
    zlib1g-dev \
    libbz2-dev \
    libreadline-dev \
    libsqlite3-dev \
    curl \
    llvm \
    libncurses5-dev \
    libncursesw5-dev \
    xz-utils \
    tk-dev \
    liblzma-dev \
    git \
    ca-certificates \
    openssh-client && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /tmp

RUN wget https://www.python.org/ftp/python/3.11.0/Python-3.11.0.tgz && \
    tar xzf Python-3.11.0.tgz && \
    cd Python-3.11.0 && \
    ./configure --enable-optimizations && \
    make -j "$(nproc)" && \
    make altinstall && \
    rm -rf /tmp/Python-3.11.0*

# pipのインストール
RUN wget https://bootstrap.pypa.io/get-pip.py && \
    python3.11 get-pip.py && \
    rm get-pip.py

RUN pip install --upgrade pip
RUN pip install --upgrade setuptools

# 作業ディレクトリの設定
WORKDIR /app

# 必要なPythonパッケージのインストール
COPY requirements.txt .
RUN python3.11 -m pip install -r requirements.txt