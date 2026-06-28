# Design — 検討用デザイン成果物

このディレクトリは **Step 1-2「静的HTMLの用意」** の成果物を置く。

> ⚠️ ここにある HTML/CSS は **本番実装ではなく、トンマナと体験を確認するための検討用イメージ**。
> 実装プラットフォーム（Shopify / Stripeスクラッチ）が決まったら、改めて本番用に作り直す。

## 構成

```
design/
├── README.md
└── mockups/
    ├── index.html          # フロント（トップページ）のイメージ
    ├── product-kunafa.html # 商品ページ（クナーファ）のイメージ
    └── assets/
        ├── css/styles.css  # トンマナを反映した共通スタイル
        └── img/            # 画像（プレースホルダ。実写真に差し替え）
```

## 見方

各 HTML をブラウザで開くだけで確認できる（ビルド不要）。

```bash
# 例：ローカルで簡易サーバを立てて確認
cd design/mockups
python3 -m http.server 8000
# → http://localhost:8000/index.html
```

## 反映しているトンマナ

[`../docs/02-tone-and-manner.md`](../docs/02-tone-and-manner.md) で定義したカラー／タイポ／余白方針を、
`assets/css/styles.css` の CSS 変数として反映している。

- カラー：深緑（Olive Green）× 生成り（Warm Cream）× 蜂蜜金（Kunafa Gold）、差し色に赤・ピスタチオ
- 見出し：セリフ／明朝、本文：サンセリフ
- ゆとりある余白、食べ物写真主役のレイアウト

## 注意

- 画像はプレースホルダ（CSSグラデーション等）で表現。実際の商品写真に差し替える前提。
- コピー（文章）は仮。確定情報・Bisanの声に合わせて調整する。
