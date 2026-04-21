# レンタル会議室予約システム

GitHub Pages + Firebase Authentication + Cloud Firestoreで構築するレンタル会議室予約システムです。

## 構成

- `index.html`: サイト本体
- `firestore.rules`: Firestore Security Rulesサンプル
- `.nojekyll`: GitHub Pages用

## 反映方法

リポジトリ直下へ以下をアップロードしてください。

- index.html
- README.md
- .nojekyll
- firestore.rules

## UID確認

GitHub Pagesを開き、会員登録またはログインします。
ログイン状態欄の「管理者設定用UID」をコピーし、Firebase ConsoleのFirestore Rulesにある `YOUR_ADMIN_UID` と置き換えます。

## 会議室マスタ登録

Firestore Rulesを公開後、サイト上の「会議室マスタを登録/更新」ボタンを押します。
