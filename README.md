# レンタル会議室予約システム

GitHub Pages + Firebase Authentication + Cloud Firestoreで構築するレンタル会議室予約システムです。

## 構成

- `index.html`: サイト本体
- `firestore.rules`: Firestore Security Rulesサンプル
- `.nojekyll`: GitHub Pages用

## 今回の実装範囲

- 会員登録・ログイン・ログアウト
- 管理者設定用UID表示
- Firestore会議室マスタ25件登録
- 会議室一覧のリアルタイム表示
- 予約登録
- 最大24時間制限
- 料金自動計算
- `room_slots` による二重予約防止
- 自分の予約一覧表示
- 予約キャンセルと時間枠解除

## 反映方法

リポジトリ直下へ以下をアップロードしてください。

- index.html
- README.md
- .nojekyll
- firestore.rules

## Firestore Rulesの注意

`firestore.rules` の `YOUR_ADMIN_UID` は、実際の管理者UIDに置き換えてからFirebase Consoleへ貼り付けてください。

すでにFirebase Console側で管理者UIDを設定済みの場合、新しいrulesに貼り替える際も同じUIDを入れてください。

## コレクション

- `rooms`: 会議室マスタ
- `reservations`: 予約本体
- `room_slots`: 二重予約防止用の時間枠ロック
- `admin_logs`: 次工程以降の管理者操作ログ用
