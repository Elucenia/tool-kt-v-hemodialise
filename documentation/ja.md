<!-- ELUCENIA technical documentation · kt-v-hemodialise · ja · no clinical/professional/rights approval -->

# 血液透析のKt/V・URR

[条件・出典・許諾](https://elucenia.org/ja/tools/kt-v-hemodialise)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 透析前尿素

`pre`

mg/dL · 範囲: 10–500

### 透析後尿素

`pos`

mg/dL · 範囲: 2–400

### 1回の時間

`horas`

時間 · 範囲: 1–10

### 除水量（減少体重）

`uf`

L (kg) · 範囲: 0–8

### 透析後体重

`peso`

kg · 範囲: 20–250

## 方法の版

Daugirdas第2世代1993：可変spKt/V；UF/透析後体重；URR；平衡Kt/Vではない

## 記載された計算式

spKt/V = −ln(R − 0.008 × t) + (4 − 3.5 × R) × UF ÷ P

R = 透析後尿素 ÷ 透析前尿素; t = 時間 (h); UF = 除水量 (L); P = 透析後体重 (kg).

URR (%) = (1 − R) × 100.

## 限界・対象集団

この式は、単一コンパートメントと体積補正を用いて一回の透析のspKt/Vを推定し、平衡Kt/Vや週当たりKt/Vと同等ではありません。試料採取の手技と時点、単位、透析処方は方法に対応する必要があります。KDOQIの目標には独自の状況と出典があり、単一の値の分析は治療全体の適切性を確定しません。

## 参考文献

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
