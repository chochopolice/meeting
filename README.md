# レンタル会議室予約システム

GitHub Pages + Firebase で作るレンタル会議室予約システムのMVPです。

## 今回の状態

- GitHub Pages用の静的サイト
- Firebase Authenticationによる会員登録・ログイン・ログアウト
- Cloud Firestore接続
- rooms コレクションへの会議室マスタ登録/更新
- Firestoreからの会議室マスタ読み込み

## ファイル

- `index.html`：サイト本体
- `.nojekyll`：GitHub Pages用
- `firestore.rules`：Firestore Security Rulesのサンプル

## Firestore Security Rules設定

1. GitHub Pagesに `index.html` を反映する
2. サイトでログインする
3. 画面の「UID」をコピーする
4. Firebase Console → Firestore Database → ルール を開く
5. `firestore.rules` の内容を貼り付ける
6. `YOUR_ADMIN_UID` をコピーしたUIDに置き換える
7. 公開する
8. サイトの「会議室マスタを登録/更新」を押す

## 登録される会議室

- 大会議室：3室、300円/時間
- 中会議室：7室、200円/時間
- 小会議室：15室、100円/時間

合計25室です。

## 次工程

- 予約登録機能
- 二重予約防止用の room_slots コレクション
- マイページの予約一覧
- 管理者による予約変更・削除・上書き
