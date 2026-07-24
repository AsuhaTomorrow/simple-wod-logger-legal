# simple-wod-logger-legal

iOS アプリ **WOD Logger** の法務関連ページを GitHub Pages で配信するリポジトリ。

## 公開 URL

| ページ | URL |
|--------|-----|
| 目次 | https://asuhatomorrow.github.io/simple-wod-logger-legal/ |
| プライバシーポリシー（日本語） | https://asuhatomorrow.github.io/simple-wod-logger-legal/privacy/ |
| Privacy Policy (English) | https://asuhatomorrow.github.io/simple-wod-logger-legal/privacy/en/ |

プライバシーポリシー（日本語）の URL は App Store Connect およびアプリの
`App/Info.plist`（`LegalPrivacyPolicyURL`）に登録される。**パスを変更すると出荷済みビルドのリンクが切れる**ため、
既存パスは変更せず、新規ページはディレクトリを追加する形で増やすこと。

## 構成

```
index.html            目次
privacy/index.html    プライバシーポリシー（日本語）
privacy/en/index.html Privacy Policy (English)
.nojekyll             Jekyll 処理をバイパス
```

各 HTML は CSS を埋め込んだ自己完結型の単一ファイル。外部リソースへの依存はない。
ライト / ダークの両テーマに対応（`prefers-color-scheme` と `data-theme` の両系統）。

## デプロイ

GitHub Pages（`main` ブランチ / root）。`main` に push すると自動でデプロイされる。
ビルドステップはなく、ファイルがそのまま配信される。

## ポリシー改定時の手順

1. 本文を更新する
2. **ヘッダの「施行日」とフッタの「最終更新」の両方**を更新する（2 箇所ある）
3. 日本語版と英語版の**両方**を同じ内容に更新する（片方だけに条項がある状態を作らない）
4. `main` に push する
