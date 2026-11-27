# チャートの文法

「チャートは、背景（スペース変換）に前景（ビジュアル変換）を重ねたもの」という考え方を、触って確かめるための教材です。授業で投影して使うことを想定しています。

公開ページ: https://grammar-of-charts.visualizing.jp/

## 場面

0. **表紙**
1. **分ける** — 一枚に見える絵が、前景と背景の2枚でできていることを見る
2. **前景をつくる** — 図形記号（点・線・面・サーフェイス・ボリューム）× 知覚チャンネル（配置・サイズ・形状・色・テクスチャ・動き）
3. **背景をえらぶ** — 同じ点を、直交・極・地理・ネットワークの4つの座標系に置く
4. **かさねる** — 9つのチャートを、背景と前景に分けて見る
5. **背景を替えると** — 前景は同じでも、背景を替えると別のチャートになることを見る

## 操作

| キー | 動き |
|---|---|
| ← → | 場面を切り替える |
| ↑ ↓ | 場面の中でえらぶ |
| Space | 動かす（分ける／かさねる、背景を替える など） |

## つくり

`index.html` ひとつで動きます。外部のライブラリや画像は読み込みません。

データは `index.html` の中に埋め込んであります。

- `data-yogurt` — ヨーグルトの栄養成分（タブ区切り）。使う列はスクリプト冒頭の `YOGURT_AXES` で指定
- `data-nightingale` — ナイチンゲールの月別死者数（カンマ区切り）
- `data-land` — 場面3の陸地の輪郭

## データの出典

- ナイチンゲールの死者数: R パッケージ HistData の `Nightingale` に由来するデータセット（[@stdlib/datasets-nightingales-rose](https://www.npmjs.com/package/@stdlib/datasets-nightingales-rose)）
- 陸地の輪郭: [Natural Earth](https://www.naturalearthdata.com/) 1:110m（[world-atlas](https://www.npmjs.com/package/world-atlas) 経由、間引き済み）
