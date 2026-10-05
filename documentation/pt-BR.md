<!-- ELUCENIA technical documentation · kt-v-hemodialise · pt-BR · no clinical/professional/rights approval -->

# Kt/V e URR na hemodiálise

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/kt-v-hemodialise)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Ureia pré-diálise

`pre`

mg/dL · intervalo: 10–500

### Ureia pós-diálise

`pos`

mg/dL · intervalo: 2–400

### Duração da sessão

`horas`

horas · intervalo: 1–10

### Ultrafiltração (peso perdido)

`uf`

L (kg) · intervalo: 0–8

### Peso pós-diálise

`peso`

kg · intervalo: 20–250

## Edição do método

Daugirdas 2ªgeração 1993:sp Kt/V variável; UF/peso pós; URR; sem Kt/Vequilibrado

## Fórmula documentada

spKt/V = −ln(R − 0,008 × t) + (4 − 3,5 × R) × UF ÷ P

R = ureia pós ÷ ureia pré; t = duração (h); UF = ultrafiltração (L); P = peso pós-diálise (kg).

URR (%) = (1 − R) × 100.

## Limites e população

Esta fórmula estima spKt/V de uma sessão, com compartimento único e correção de volume, e não equivale ao Kt/V equilibrado ou semanal. A técnica e o momento das amostras, unidades e regime de diálise precisam corresponder ao método. Metas KDOQI têm contexto e fonte próprios; a análise do valor isolado não confirma adequação global do tratamento.

## Referências

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
