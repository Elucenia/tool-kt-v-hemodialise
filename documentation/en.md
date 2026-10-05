<!-- ELUCENIA technical documentation · kt-v-hemodialise · en · no clinical/professional/rights approval -->

# Kt/V and URR in hemodialysis

[conditions, sources and permissions](https://elucenia.org/en/tools/kt-v-hemodialise)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Predialysis urea

`pre`

mg/dL · range: 10–500

### Postdialysis urea

`pos`

mg/dL · range: 2–400

### Session duration

`horas`

hours · range: 1–10

### Ultrafiltration (weight lost)

`uf`

L (kg) · range: 0–8

### Postdialysis weight

`peso`

kg · range: 20–250

## Method edition

Daugirdas second generation 1993: variable-volume spKt/V; UF/post weight; URR; not equilibrated Kt/V

## Documented formula

spKt/V = −ln(R − 0.008 × t) + (4 − 3.5 × R) × UF ÷ P

R = post urea ÷ pre urea; t = duration (h); UF = ultrafiltration (L); P = post-dialysis weight (kg).

URR (%) = (1 − R) × 100.

## Limits and population

This formula estimates single-session spKt/V with a single compartment and volume correction; it is not equivalent to equilibrated or weekly Kt/V. Sampling technique and timing, units and dialysis regimen must match the method. KDOQI targets have their own context and source; analysis of the value alone does not confirm overall treatment adequacy.

## References

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
