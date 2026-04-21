# レンタル会議室予約システム

GitHub Pages + Firebase Authentication + Cloud Firestore で動作するレンタル会議室予約サイトです。

## 今回の内容

- 会員登録・ログイン
- 会議室マスタ登録
- 予約登録
- room_slots による二重予約防止
- 全会議室の空き状況カレンダー
- 自分の予約一覧・キャンセル
- 管理者画面
  - 全予約一覧
  - 予約変更
  - 管理者キャンセル
  - 緊急上書き予約
  - 操作ログ登録
- 通常ユーザー画面から Firestore 会議室マスタ表示を非表示化
- 大会議室カードの pill 表示を拡大

## 反映方法

GitHubリポジトリ直下に以下を上書きしてください。

- index.html
- firestore.rules
- README.md
- .nojekyll

その後、Firebase Console の Firestore Database > ルール に `firestore.rules` の内容を貼り付けて公開してください。

## 管理者UID

現在の管理者UID:

```text
vgW29wAqLeTATkfgq6iGj0agpBT2
```

## 注意

管理者画面は、上記UIDのユーザーでログインした場合だけ表示されます。
