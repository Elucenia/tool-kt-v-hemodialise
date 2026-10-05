<!-- ELUCENIA technical documentation · kt-v-hemodialise · it · no clinical/professional/rights approval -->

# Kt/V e URR in emodialisi

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/kt-v-hemodialise)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Urea predialisi

`pre`

mg/dL · intervallo: 10–500

### Urea postdialisi

`pos`

mg/dL · intervallo: 2–400

### Durata della sessione

`horas`

ore · intervallo: 1–10

### Ultrafiltrazione (peso perso)

`uf`

L (kg) · intervallo: 0–8

### Peso dopo dialisi

`peso`

kg · intervallo: 20–250

## Edizione del metodo

Daugirdas 2ª generazione 1993: spKt/V variabile; UF/peso post; URR; non Kt/V equilibrato

## Formula documentata

spKt/V = −ln(R − 0,008 × t) + (4 − 3,5 × R) × UF ÷ P

R = urea post ÷ urea pre; t = durata (h); UF = ultrafiltrazione (L); P = peso postdialisi (kg).

URR (%) = (1 − R) × 100.

## Limiti e popolazione

Questa formula stima lo spKt/V di una sessione, con un unico compartimento e correzione del volume; non equivale al Kt/V equilibrato o settimanale. Tecnica e momento del campionamento, unità e regime di dialisi devono corrispondere al metodo. Gli obiettivi KDOQI hanno un contesto e una fonte propri; l’analisi del solo valore non conferma l’adeguatezza complessiva del trattamento.

## Riferimenti

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
