<!-- ELUCENIA technical documentation · kt-v-hemodialise · es · no clinical/professional/rights approval -->

# Kt/V y URR en hemodiálisis

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/kt-v-hemodialise)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Urea prediálisis

`pre`

mg/dL · intervalo: 10–500

### Urea posdiálisis

`pos`

mg/dL · intervalo: 2–400

### Duración de la sesión

`horas`

horas · intervalo: 1–10

### Ultrafiltración (peso perdido)

`uf`

L (kg) · intervalo: 0–8

### Peso después de la diálisis

`peso`

kg · intervalo: 20–250

## Edición del método

Daugirdas 2ª generación 1993: spKt/V variable; UF/peso pos; URR; sin Kt/V equilibrado

## Fórmula documentada

spKt/V = −ln(R − 0,008 × t) + (4 − 3,5 × R) × UF ÷ P

R = urea pos ÷ urea pre; t = duración (h); UF = ultrafiltración (L); P = peso posdiálisis (kg).

URR (%) = (1 − R) × 100.

## Límites y población

Esta fórmula estima el spKt/V de una sesión, con compartimento único y corrección de volumen; no equivale al Kt/V equilibrado ni semanal. La técnica y el momento de las muestras, las unidades y el régimen de diálisis deben corresponder al método. Las metas KDOQI tienen su propio contexto y fuente; analizar el valor aislado no confirma la adecuación global del tratamiento.

## Referencias

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

spKt/V ≥ 1,4: alcanza el objetivo de KDOQI 2015

| Detalles del resultado | |
| --- | --- |
| Tasa de reducción de la urea (URR) | 70,0% |
| Relación pos/pre (R) | 0,300 |


### 2

spKt/V entre 1,2 y 1,4: por encima del mínimo, por debajo del objetivo

| Detalles del resultado | |
| --- | --- |
| Tasa de reducción de la urea (URR) | 65,0% |
| Relación pos/pre (R) | 0,350 |


### 3

spKt/V < 1,2: diálisis inadecuada

| Detalles del resultado | |
| --- | --- |
| Tasa de reducción de la urea (URR) | 60,0% |
| Relación pos/pre (R) | 0,400 |

URR por debajo de 65%.

