# Novel Writer - PWA小説執筆ツール

ローカル環境で動作する小説執筆ツールです。オフラインで使用でき、PWAとしてスマホのホーム画面に追加できます。

## GitHub Pagesへのデプロイ方法

### 1. リポジトリの作成
```bash
# 新しいリポジトリを作成
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/novel-writer.git
git push -u origin main
```

### 2. GitHub Pagesの有効化
1. GitHubのリポジトリページへ移動
2. Settings → Pages
3. Source: `main` branch を選択
4. Save

### 3. アイコン画像の準備（オプション）
`icon-192.png` と `icon-512.png` を用意してください。
現在はSVGアイコン（icon.svg）が含まれていますが、PNGに変換することを推奨します。

オンラインツールで変換: https://www.aconvert.com/image/svg-to-png/

### 4. アクセス
デプロイ後、`https://YOUR_USERNAME.github.io/novel-writer/novel-writer.html` でアクセスできます。

## PWAとしてインストール

### Android
1. ブラウザでサイトを開く
2. メニュー → 「ホーム画面に追加」
3. アプリとして起動可能

### iOS
1. Safariでサイトを開く
2. 共有ボタン → 「ホーム画面に追加」
3. アプリとして起動可能

## 機能
- ✅ オフライン動作
- ✅ localStorageで自動保存
- ✅ テーマ・プロット・登場人物・世界観管理
- ✅ 原稿執筆（没入モード対応）
- ✅ ダークモード
- ✅ JSON形式でエクスポート/インポート
- ✅ レスポンシブデザイン（分割ビュー対応）

## ファイル構成
```
novel-writer/
├── novel-writer.html  # メインアプリ
├── manifest.json      # PWA設定
├── sw.js             # Service Worker
├── icon.svg          # アイコン（SVG）
├── icon-192.png      # アイコン 192x192（要作成）
├── icon-512.png      # アイコン 512x512（要作成）
└── README.md         # このファイル
```

## 注意事項
- GitHub Pagesは静的ファイルのみホスト可能
- 全てのデータはブラウザのlocalStorageに保存されます
- ブラウザのデータを削除すると作品データも消えるため、定期的にエクスポートしてバックアップを取ってください

## ライセンス
MIT License
