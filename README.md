# Bisan EC

パレスチナ料理店 **Bisan（ビサン）** のECサイトプロジェクト。

東京・十条発のパレスチナ料理店 Bisan（[bisan.biz](https://bisan.biz)）が、
パレスチナの伝統菓子をはじめとする商品をオンラインで届けるためのECサイトを構築します。

## 最初の商品

パレスチナの伝統的なお菓子 **クナーファ（Kunafa / كنافة）** の冷凍販売からスタートします。
将来的には他の商品（スパイス、食材、ギフトセットなど）への拡張を見据えています。

## プロジェクトの進め方（Step 1）

本リポジトリは現在 **Step 1（企画・検討フェーズ）** にあります。

1. **トンマナの作成** — Bisanの世界観を調査し、ブランドのトーン&マナーを定義する
   → [`docs/01-brand-research.md`](docs/01-brand-research.md) / [`docs/02-tone-and-manner.md`](docs/02-tone-and-manner.md)
2. **静的HTMLの用意** — フロント／商品ページの検討用イメージを作成（本番用ではない）
   → [`design/mockups/`](design/mockups/)
3. **プラットフォームの検討** — Shopify（Shopify CLI）か Stripe活用のスクラッチ構築かを比較検討
   → [`docs/03-platform-comparison.md`](docs/03-platform-comparison.md)

## ディレクトリ構成

```
Bisan-ec/
├── README.md                  # 本ファイル
├── docs/                      # 企画・検討ドキュメント
│   ├── 00-overview.md         # プロジェクト概要・ロードマップ
│   ├── 01-brand-research.md   # Bisanの世界観調査
│   ├── 02-tone-and-manner.md  # トーン&マナー定義
│   ├── 03-platform-comparison.md  # プラットフォーム比較
│   ├── 04-product-kunafa.md   # 商品（クナーファ）情報・要件
│   └── 05-keyvisual-prompts.md # キービジュアル生成プロンプト集（Gemini向け）
└── design/                    # デザイン検討用の成果物
    ├── README.md
    └── mockups/               # 静的HTMLモックアップ（検討用）
        ├── index.html         # フロント（トップページ）
        ├── product-kunafa.html # 商品ページ
        └── assets/
            ├── css/styles.css
            └── img/
```

## ステータス

| フェーズ | 内容 | 状態 |
| --- | --- | --- |
| Step 1-1 | トンマナ作成（世界観調査） | 🟡 ドラフト |
| Step 1-2 | 静的HTMLモック | 🟡 ドラフト |
| Step 1-3 | プラットフォーム検討 | 🟡 ドラフト |

> ⚠️ 本リポジトリのドキュメント内のブランド情報は、公開記事・検索情報を基にまとめた**暫定版**です。
> 確定にはBisan関係者（シェフ・運営）への確認が必要です。詳細は各ドキュメント内の注記を参照してください。
