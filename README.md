# レンタル会議室予約システム GitHub Pages版

GitHub Pagesで公開するための最初の静的ページです。

## ファイル構成

```text
rental-meeting-room-site/
├── index.html
├── README.md
└── .nojekyll
```

## 公開手順

1. GitHubで新しいリポジトリを作成します。
2. `index.html`、`README.md`、`.nojekyll` をリポジトリ直下へアップロードします。
3. GitHubのリポジトリ画面で `Settings` を開きます。
4. 左メニューの `Pages` を開きます。
5. `Build and deployment` の `Source` を `Deploy from a branch` にします。
6. `Branch` を `main`、フォルダを `/ (root)` にして `Save` します。
7. 数分後、GitHub PagesのURLで公開されます。

## 次に実装する予定

- Firebase Authenticationによる会員登録・ログイン
- Cloud Firestoreへの会議室マスタ登録
- 予約登録機能
- 二重予約防止用の時間枠ロック
- 予約カレンダーのリアルタイム反映
- 管理者画面
