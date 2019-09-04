# 起動方法

## 前提条件
- git (Git Bash を推奨)
- Docker for windows
- Docker toolbox
のインストール

### 参考資料
[Git bashインストール](https://qiita.com/toshi-click/items/dcf3dd48fdc74c91b409)
[Docker, Docker toolboxのインストール](https://qiita.com/maemori/items/52b1639fba4b1e68fccd)
[makeコマンドのインストール](https://qiita.com/tokikaze0604/items/e13c04192762f8d4ec85)

## 推奨条件
- Git Hubのユーザー登録
- DockerHubのユーザー登録
- コマンドラインの知識
- makeコマンドのインストール

## 実際の操作
1. gitでこのプロジェクトをクローンして、プロジェクトディレクトリに入る。
  `git clone https://github.com/NNN-kakimoto/seed_php.git`
2. 【初回のみ】Dockerコンテナを生成する。
  `docker-compose build`
3. Dockerコンテナを立ち上げる。
  `docker-compose up -d`
4. ページを確認する。
  - インストールしたDocker toolboxのソフトウェア「Kitematic」で左ペインに並ぶコンテナ一覧から、apache-phpとあるのを確認する。
  - 【初回のみ】apache-phpを選び、右上のsettingsタブを選択。Networkの設定項目の中の、「CONNECT TO HOST　NETWORK」ボタンを押す。
  - 【初回のみ】左ペインのコンテナに緑のアイコンがつくのを確認。
  - php のコンテナを選択し右側の「WEB PREVIEW」を押すと、ブラウザでそのページを開くことができる。
5. 作業を開始する。

# 各種コマンド
- 一括で立ち上げ
  `docker-compose up -d`
  `-d`を外すとリアルタイムでログが見れる。離脱する場合はctrl+cだが、押すとサービスごと落ちるので再度upする必要があるので注意。
- 一括でサービス停止
  `docker-compose down`
- 起動状態の確認
  `docker-compose ps`
  サービスが起動して正常に動いている状態であれば、