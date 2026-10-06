<!-- ELUCENIA technical documentation · kt-v-hemodialise · de · no clinical/professional/rights approval -->

# Kt/V und URR bei Hämodialyse

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/kt-v-hemodialise)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Harnstoff vor Dialyse

`pre`

mg/dL · Bereich: 10–500

### Harnstoff nach Dialyse

`pos`

mg/dL · Bereich: 2–400

### Dauer der Einheit

`horas`

Stunden · Bereich: 1–10

### Ultrafiltration (Gewichtsverlust)

`uf`

L (kg) · Bereich: 0–8

### Gewicht nach Dialyse

`peso`

kg · Bereich: 20–250

## Fassung der Methode

Daugirdas 2. Generation 1993: variables spKt/V; UF/Gewicht nach Dialyse; URR; kein äquilibriertes Kt/V

## Dokumentierte Formel

spKt/V = −ln(R − 0,008 × t) + (4 − 3,5 × R) × UF ÷ P

R = Harnstoff nach ÷ Harnstoff vor; t = Dauer (h); UF = Ultrafiltration (L); P = Gewicht nach Dialyse (kg).

URR (%) = (1 − R) × 100.

## Grenzen und Population

Diese Formel schätzt den spKt/V einer Sitzung mit einem Kompartiment und Volumenkorrektur und entspricht nicht dem äquilibrierten oder wöchentlichen Kt/V. Technik und Zeitpunkt der Proben, Einheiten und Dialyseregime müssen zur Methode passen. KDOQI-Ziele haben eigenen Kontext und Quelle; der isolierte Wert bestätigt keine umfassende Behandlungsadäquanz.

## Referenzen

- [Daugirdas JT. Second generation logarithmic estimates of single-pool variable volume Kt/V: an analysis of error. J Am Soc Nephrol, 1993.](https://doi.org/10.1681/ASN.V451205)

- [National Kidney Foundation. KDOQI Clinical Practice Guideline for Hemodialysis Adequacy: 2015 Update. Am J Kidney Dis, 2015.](https://doi.org/10.1053/j.ajkd.2015.07.015)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

spKt/V ≥ 1,4: erreicht das KDOQI-2015-Ziel

| Ergebnisdetails | |
| --- | --- |
| Harnstoff-Reduktionsrate (URR) | 70,0 % |
| Post/Prä-Verhältnis (R) | 0,300 |


### 2

spKt/V zwischen 1,2 und 1,4: über dem Mindestwert, unter dem Zielwert

| Ergebnisdetails | |
| --- | --- |
| Harnstoff-Reduktionsrate (URR) | 65,0 % |
| Post/Prä-Verhältnis (R) | 0,350 |


### 3

spKt/V < 1,2: unzureichende Dialyse

| Ergebnisdetails | |
| --- | --- |
| Harnstoff-Reduktionsrate (URR) | 60,0 % |
| Post/Prä-Verhältnis (R) | 0,400 |

URR unter 65 %.

