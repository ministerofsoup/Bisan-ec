# キービジュアル生成プロンプト集（Gemini向け）

> サイト掲載用のキービジュアルを画像生成AI（Gemini / Imagen など）で作るためのプロンプト集。
> トンマナは [`02-tone-and-manner.md`](02-tone-and-manner.md) に準拠（深緑 × 生成り × 蜂蜜金、本場・温かさ・手仕事・敬意）。
> 生成画像は `design/mockups/assets/img/` に配置し、モックのプレースホルダと差し替える。

## 使い方の共通ルール

- **テキストは画像に入れない**（見出しはサイト側のフォントで重ねる）。各プロンプトに `No text` を明記。
- **一貫性**：気に入った1枚ができたら、その画像を添付して「同じスタイル・ライティングで」と指示すると他カットが揃う。
- **縦横比**：各プロンプトの比率はモックのCSSスロットに合わせている。
- **ファイル名の目安**：`hero.jpg` / `story.jpg` / `kunafa-main.jpg` / `kunafa-1〜4.jpg` / `card-kunafa.jpg`

---

## A. ヒーロー背景（トップ最上部・風景）

トップの「パレスチナの食卓を、ご自宅へ。」の**裏に敷く風景画像**。
文字を重ねる前提で、中央〜上部はうるさくせず、緑のスクリム（暗幕）と馴染むトーンに。

> 実装メモ：ヒーローは画像の上に深緑の半透明オーバーレイ＋下部の暗幕＋文字影を重ねている
> （`assets/css/styles.css` の `.hero`）。`assets/img/hero.jpg` を置くと自動で背景に出る。

### 風景用・共通スタイル基盤（末尾に貼る）

```
Style: cinematic landscape photography, warm golden-hour light, soft haze,
timeless and serene, gentle film-like grading, high detail, no people in focus.
Palette leaning to olive green, warm cream, honey gold, soft terracotta.
Composition: calm and balanced, with smooth uncluttered areas in the center
and upper-middle so overlaid text stays legible; darker tones toward edges.
No text, no logos, no watermarks, no modern buildings or vehicles. Photorealistic.
Aspect ratio 16:9.
```

### A-1. 本命：オリーブ畑と段々の丘（黄金の光）

```
A tranquil Palestinian countryside at golden hour: ancient olive groves on
gently terraced hills, silvery-green olive leaves, dry-stone terraces,
rolling Mediterranean landscape fading into warm hazy distance.
Soft warm sunlight, long calm shadows, peaceful and nostalgic atmosphere.
[+ 風景用・共通スタイル基盤]
```

### A-2. 古都の趣：石造りの町並みと丘（店名Bisanの故郷を想起）

```
A timeless Middle Eastern hillside town at dusk: old sand-colored stone houses
and arches built into a terraced slope, olive trees scattered around,
distant hills under a soft warm sky. Quiet, historic, heartfelt mood.
Warm earthy tones harmonizing with olive green.
[+ 風景用・共通スタイル基盤]
```

### A-3. 質感重視：手前にオリーブの枝、奥に丘（ボケ）

文字が乗る中央を空けやすく、最も背景向き。

```
Close foreground of an olive tree branch with leaves and a few green olives on
the left side, softly blurred terraced Palestinian hills and warm sky filling
the rest of the frame with smooth bokeh. Shallow depth of field, airy negative
space across the center for text overlay. Warm golden afternoon light.
[+ 風景用・共通スタイル基盤]
```

> **スマホ用（縦長）**：同じ画で末尾の `Aspect ratio 16:9` を `Aspect ratio 4:5`（または `9:16`）に変えてもう1枚生成すると、縦画面での見切れを防げる。

---

## B. 食べ物・商品系キービジュアル

### 食べ物用・共通スタイル基盤（末尾に貼る）

```
Style: warm natural daylight, soft shadows, authentic and handcrafted feel,
editorial food photography, shallow depth of field, gentle film-like color grading.
Color palette: warm cream (#F7F1E6), deep olive green (#1E5631),
honey gold (#D98A2B), pistachio green (#7BA05B).
Mood: heartfelt, traditional Palestinian hospitality, premium but unpretentious.
No text, no logos, no lettering, no watermarks. Photorealistic.
```

### B-1. ストーリー用ビジュアル（4:3）— `story.jpg`

```
Close-up of hands preparing traditional Palestinian kunafa in a warm kitchen,
brushing syrup over crispy golden kataifi pastry, pistachios nearby in a small
brass bowl. Authentic, intimate, documentary feel. Warm window light.
[+ 食べ物用・共通スタイル基盤]  Aspect ratio 4:3.
```

### B-2. 商品メイン写真（1:1）— `kunafa-main.jpg`

```
A single serving of Palestinian kunafa on a small plate, hero product shot,
golden crispy kataifi exterior, melted cheese stretching as a piece is lifted
with a fork, bright green pistachio garnish, drizzle of honey syrup.
Centered composition, clean warm cream background, appetizing and luxurious.
[+ 食べ物用・共通スタイル基盤]  Aspect ratio 1:1.
```

### B-3. 商品サブ写真（1:1 ×4）— `kunafa-1.jpg`〜`kunafa-4.jpg`

```
1) Macro top-down of kunafa surface, crispy golden strands and pistachio dust.
2) Cross-section of kunafa showing molten cheese layer inside golden pastry.
3) Frozen kunafa portion on parchment, ready-to-ship packaging style, clean.
4) Kunafa being warmed, steam rising, honey syrup poured from a small jug.
[各カットに + 食べ物用・共通スタイル基盤]  Aspect ratio 1:1.
```

### B-4. 商品カードのサムネ（4:3）— `card-kunafa.jpg`

```
Appetizing kunafa slice on a rustic plate, top-down, minimal styling,
plenty of warm cream negative space around the dish for a clean card look.
[+ 食べ物用・共通スタイル基盤]  Aspect ratio 4:3.
```

### B-5（任意）ブランドの世界観カット（3:2）

```
An inviting Palestinian table setting seen from above: kunafa, small cups of
Arabic coffee, fresh mint, dates, olive branch, on a hand-embroidered tatreez
textile with subtle geometric patterns in olive green and red.
Warm, festive, welcoming.
[+ 食べ物用・共通スタイル基盤]  Aspect ratio 3:2.
```

---

## C. 文化モチーフの扱い（要・運営確認）

実店舗はパレスチナ国旗・地図など文化的アイコンを掲げているが、EC キービジュアルは
まず「食 × ぬくもり × 風景」を主役にする方針。国旗等の明示的な政治的モチーフは
シェフ・運営の意向確認のうえ判断する。

- 控えめに文化色を足したい場合の追記例：
  `Subtly include Palestinian cultural motifs (tatreez embroidery patterns) in the background, tasteful and respectful, not a flag.`

---

## D. 生成後の差し替え手順（メモ）

1. 生成画像を `design/mockups/assets/img/` に上記ファイル名で配置。
2. ヒーローは `hero.jpg` を置くだけで背景に反映（CSS実装済み）。
3. その他のスロット（story / 商品 / カード）は、CSSのグラデーション面を
   `<img>` または `background-image` に置き換えてコミット＆再デプロイ。
4. 明るすぎて文字が読みにくい場合は `.hero` のスクリム濃度を調整。
