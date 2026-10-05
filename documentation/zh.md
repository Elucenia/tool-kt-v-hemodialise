<!-- ELUCENIA technical documentation · kt-v-hemodialise · zh · no clinical/professional/rights approval -->

# 血液透析中的 Kt/V 与 URR

[条件、来源与许可](https://elucenia.org/zh/tools/kt-v-hemodialise)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 透析前尿素

`pre`

mg/dL · 范围: 10–500

### 透析后尿素

`pos`

mg/dL · 范围: 2–400

### 每次持续时间

`horas`

小时 · 范围: 1–10

### 超滤量（减少的体重）

`uf`

L (kg) · 范围: 0–8

### 透析后体重

`peso`

kg · 范围: 20–250

## 方法版本

Daugirdas第2代1993：可变容量spKt/V；UF/透析后体重；URR；非平衡Kt/V

## 已记录的公式

spKt/V = −ln(R − 0.008 × t) + (4 − 3.5 × R) × UF ÷ P

R = 透析后尿素 ÷ 透析前尿素; t = 时长 (h); UF = 超滤量 (L); P = 透析后体重 (kg).

URR (%) = (1 − R) × 100.

## 限制与适用人群

此公式以单室模型及容积校正估计一次透析的spKt/V，并不等同于平衡Kt/V或每周Kt/V。采样技术与时间、单位及透析方案须与方法一致。KDOQI目标具有各自的情境与来源；单独分析该值不能确认整体治疗充分性。

## 参考文献

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
