# レンタル会議室予約システム

GitHub Pages + Firebase Authentication で動く、レンタル会議室予約サイトの初期版です。

## 現在できること

- トップページ表示
- 会議室料金表示
- 予約フォームのデモ表示
- Firebase Authentication による会員登録
- Firebase Authentication によるログイン
- ログアウト
- ログイン状態の画面反映

## まだ未実装のこと

- Firestore への会議室マスタ登録
- Firestore への予約登録
- 二重予約防止
- 会議室ごとのリアルタイムカレンダー
- マイページ
- 管理者画面

## GitHub Pages への反映

1. このフォルダの `index.html`、`README.md`、`.nojekyll` をリポジトリ直下へアップロードします。
2. GitHub の `Settings` → `Pages` を開きます。
3. Source を `Deploy from a branch` にします。
4. Branch を `main`、フォルダを `/ (root)` にします。
5. 数分後に公開URLへアクセスします。

## Firebase Authentication の注意

GitHub Pages のURLでログインエラーが出る場合は、Firebase Consoleで以下を確認してください。

Authentication → Settings → Authorized domains

ここに GitHub Pages のドメインを追加します。

例：

- chochopolice.github.io

## 次の工程

次は Cloud Firestore を接続し、会議室マスタと予約登録機能を追加します。
