# ハコミセラピー LP デザイン設計

## コンセプト

「静かな専門性」を中心に、情緒から理解、安心、低圧CTAへ進む構成です。既存サイトの白背景・えんじ系見出し・素朴で温かい印象に寄せながら、LPとしての読みやすさと申込導線を整理しています。

## セクション構造

1. ファーストビュー: キャッチ、サブコピー、説明会・資料請求CTA、信頼要素、静かなビジュアル
2. 導入: 臨床家としての在り方を深める学びであることを提示
3. 問題提起: 圧迫感のないチェックリスト
4. ハコミとは: 身体志向、マインドフルネス、非暴力性、関係性の図解
5. 支持される理由: 4カードで臨床変化を提示
6. 他療法との違い: CBT、EMDR、IFS、Focusing/SEとの補完性比較
7. 受講後の変化: Before/After
8. 受講生の声: 職業、実感、臨床変化
9. トレーニング内容: 基礎、体験、実践、国際認定
10. トレーナー紹介: 人柄と学習環境
11. FAQ: 不安解消
12. 最終CTA: 「まずは知る」導線

## PC版LPデザイン

- 最大幅: `1180px`
- ファーストビュー: 左にコピー、右に縦長ビジュアル
- 問題提起・プログラム: 左固定見出し、右に本文コンテンツ
- 比較表: 3カラムで補完性を一覧化
- 受講生の声: 3カラムカード
- 最終CTA: 中央配置で低圧導線

## モバイル版LPデザイン

- すべて1カラム化
- ヘッダーナビは非表示、説明会CTAのみ残す
- CTAボタンは全幅化
- 比較表は行ごとのカード表示
- 画像は高さを抑えて、スクロール疲れを軽減

## ワイヤーフレーム

PC:

```text
[Header: Brand | Nav | CTA]

[Hero]
  [Copy / Lead / CTA / Trust strip]   [Quiet visual]

[Intro]
  [Section title]                     [Long body copy]

[Issue]
  [Sticky heading]                    [Quiet checklist]

[About]
  [Centered heading]
  [Large concept map]
  [4 principle cards]

[Reasons] [4 cards]
[Comparison table]
[Before / After]
[Voices: 3 cards]
[Program: heading + timeline]
[Trainer: image + philosophy]
[FAQ]
[Final CTA]
```

Mobile:

```text
[Header: Brand | CTA]
[Hero copy]
[CTA buttons]
[Trust strip]
[Quiet visual]
[Intro]
[Issue checklist]
[About map]
[Cards stacked]
[Comparison cards]
[Before]
[After]
[Voices stacked]
[Timeline]
[Trainer]
[FAQ]
[Final CTA]
```

## UIコンポーネント

- ヘッダー: 透明感のある固定ヘッダー、低圧CTA
- CTAボタン: 深いえんじのプライマリ、白背景のセカンダリ
- チェックリスト: 小さな円形マーカーで静かに提示
- カード: 8px角丸、薄い罫線、余白広め
- 比較表: PCは3カラム、モバイルはカード化
- Timeline: 数字マーカー付き縦流れ
- FAQ: native details/summary

## 配色

- Base: `#fffdf8`, `#f7efe4`, `#ffffff`
- Text: `#3b2b26`, `#71635c`
- Accent: `#64110d`, `#9a725b`, `#9b6947`
- Line: `#e2d4c5`

既存サイトのえんじ・茶系の印象に寄せ、彩度を落とした生成り背景で落ち着きを出しています。CTAもギラつかせず、既存サイトの見出し色に近い深いえんじで統一しています。

## タイポグラフィ

- 見出し: `Hiragino Mincho ProN`, `Yu Mincho`, `Noto Serif JP`
- 本文: `Hiragino Kaku Gothic ProN`, `Hiragino Sans`, `Yu Gothic`, `Noto Sans JP`
- 行間: 本文は `1.9` を基準に広め

## CTA配置

- ファーストビュー: 無料説明会、資料請求
- ヘッダー: 説明会への固定導線
- 最終CTA: 無料説明会、資料請求、問い合わせ

## 画像方針

現状の実装では、ストックフォト感を避けるために静かな抽象ビジュアルをローカル画像アセットとして配置しています。実運用時は自然光、対話、沈黙、安心感、柔らかな表情を感じる写真に差し替える前提です。

推奨差し替え箇所:

- `assets/hero-visual.png`: ファーストビューの対話・呼吸感ビジュアル
- `assets/voice-1.png` から `assets/voice-3.png`: 受講生の声の顔写真
- `assets/trainer-visual.png`: トレーナー紹介写真

## 実装ファイル

- `index.html`
- `styles.css`
