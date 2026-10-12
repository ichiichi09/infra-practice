#FROM：ビルドが拡張するベースイメージを指定します。　Dockerイメージを作るときに、Node.js 22が使える既存のイメージを土台にする」
FROM node:22
#WORKDIR：コンテナ内の作業ディレクトリを指定
WORKDIR /app
#COPY：ファイルをコンテナ内にコピー
COPY package*.json ./
#RUN：イメージを作る段階でコマンドを実行　今回で言うとexpress
RUN npm install
COPY . .
#CMD：コンテナ起動時に実行するコマンドを指定
CMD ["node", "server.js"]

#RUN はイメージの準備、CMD はコンテナ起動時の処理