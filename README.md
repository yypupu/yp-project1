# Y-PU プロジェクト運営アプリ

Y-PU ENTERTAINMENT の学生プロジェクト運営アプリ（ToDo・集客アタック・メンバー表・備品表・制作物・資料・タイムテーブル・アンケート分析・権限）。

## しくみ

| 部分 | 場所 | 役割 |
|---|---|---|
| データ | Googleスプレッドシート（マスター） | すべての記録の保管場所 |
| 処理 | Google Apps Script（スプレッドシートに紐づけ） | ログイン、保存、メール送信、フォーム取り込み、権限チェック |
| 画面 | GitHub Pages（このリポジトリの `index.html`） | 表示だけ。データは含まない |

## ファイル

- `index.html` … GitHub Pages で表示する画面
- `config.js` … Apps Script のウェブアプリURL（`…/exec`）を1行書くファイル
- `gas/コード.gs` … Apps Script の「コード.gs」に貼るコード
- `gas/Index.html` … Apps Script の「Index.html」に貼る画面（Apps ScriptのURLから直接開くとき用）

## 更新のしかた

1. 画面を変えたとき：`index.html` と `gas/Index.html` を差し替える
2. 仕組みを変えたとき：`gas/コード.gs` を Apps Script に貼る →「Y-PUアプリ → 初期チェック」→「デプロイを管理 → 新バージョン」（Y-PUのアカウントで）
3. `config.js` のURLは、デプロイを「新バージョン」で更新する限り変わらない

## 公開設定

- Apps Script のデプロイ：次のユーザーとして実行「自分（Y-PU）」、アクセスできるユーザー「全員」
- GitHub Pages：Settings → Pages → Branch `main` / `(root)`
