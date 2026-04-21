# レンタル会議室予約システム

GitHub Pages + Firebase Authentication + Cloud Firestoreで構築するレンタル会議室予約システムです。

## 構成

- `index.html`: サイト本体
- `firestore.rules`: Firestore Security Rules
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
- 選択日の空き状況表示
- 全会議室の空き状況カレンダー
- 会議室種別フィルター
- 空き枠クリックで予約フォームへ反映
- 自分の予約一覧表示
- 予約キャンセルと時間枠解除

## 反映方法

リポジトリ直下へ以下をアップロードしてください。

- index.html
- README.md
- .nojekyll
- firestore.rules

GitHub Pages反映後、ブラウザで `Ctrl + F5` を押して強制更新してください。

## Firestore Rulesの注意

今回の `firestore.rules` には、管理者UIDとして以下を設定済みです。

```text
vgW29wAqLeTATkfgq6iGj0agpBT2
```

Firebase Console の Firestore Database → ルール に貼り付けて公開してください。

## コレクション

- `rooms`: 会議室マスタ
- `reservations`: 予約本体
- `room_slots`: 二重予約防止用の時間枠ロック
- `admin_logs`: 次工程以降の管理者操作ログ用
