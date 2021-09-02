# ベースイメージ指定
FROM golang:latest

# ワークディレクトリを指定
WORKDIR /app

# ホストOSのapps内全てをWORKDIRにコピー
COPY . ./

# ビルド
RUN go build -o ./server-run ./server

# コンテナのポートを9090で公開
EXPOSE 9090

# アプリ実行
CMD [ "./server-run" ]