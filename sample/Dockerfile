# golang のイメージを取得
FROM golang:1.13.3

WORKDIR /go
ADD . /go

RUN go get -u -v github.com/labstack/echo/...


# ソースのコピー先
ENV SRC_DIR=/go/src/github.com/sample


## key=val形式で複数の環境変数を定義
# GOBIN: bin
# GOSRC: src
# ...
ENV GOBIN=/go/bin  \
    GOSRC=/go/src


# RUN, や ENTRYPOINT などを実行するワークディレクトリを指定
WORKDIR $GOBIN

# ソースをコピーする
# ADD . $SRC_DIR

# コンパイル
WORKDIR $GOSRC

# echoインストール

# RUN go install github.com/sample/app;

# プログラム実行
# ENTRYPOINT ["./sample"]

# 8080 ポートを解放
EXPOSE 8080