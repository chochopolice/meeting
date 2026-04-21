# レンタル会議室予約システム

GitHub Pages + Firebase Authentication + Cloud Firestore で動作するレンタル会議室予約サイトです。

## 今回の内容

- Firestore Security Rules の強化
- `room_slots` に予約者UIDを追加
- ユーザーは自分の予約・自分の予約枠だけ操作可能
- 管理者は全予約・全予約枠・会議室マスタ・操作ログを管理可能
- 予約の作成時に、会議室種別・料金・利用時間・ステータスをルール側でも検証
- 通常ユーザーの予約更新は「キャンセル」に限定
- 管理者UIDを反映済み

## 反映方法

GitHubリポジトリ直下に以下を上書きしてください。

- `index.html`
- `firestore.rules`
- `README.md`
- `.nojekyll`

その後、Firebase Console の Firestore Database > ルール に `firestore.rules` の内容を貼り付けて公開してください。

## 管理者UID

```text
vgW29wAqLeTATkfgq6iGj0agpBT2
```

## 注意

今回から新規作成される `room_slots` には `userId` が入ります。過去のテスト予約で作成された古い `room_slots` に `userId` がない場合、通常ユーザーのキャンセル時に権限エラーになることがあります。その場合は管理者画面からキャンセルしてください。
