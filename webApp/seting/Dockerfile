# golang のイメージを取得
FROM golang:1.13.3

## key=val形式で複数の環境変数を定義
# GOBIN: bin
# GOSRC: src
# GOAPP: app
# ...
ENV GOBIN=/go/bin  \
    GOSRC=/go/src  \
    GOAPP=/go/app


RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "vim"]

# 実行するワークディレクトリを指定
# "docker-compose.yml"が入っているフォルダーのコピー先
WORKDIR /go
ADD . /go/seting/

# echoインストール
# RUN go get -u -v github.com/labstack/echo/...




# 実行するワークディレクトリを指定
#  RUN, ENTRYPOINT, CMDなどでプログラム実行
WORKDIR $GOAPP
RUN makdir app
CMD ["./app"]

# 80 ポートを解放
EXPOSE 80