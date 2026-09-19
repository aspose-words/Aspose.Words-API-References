---
title: "Enum Aspose::Words::Math::MathObjectType"
linktitle: "MathObjectType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Math::MathObjectType. Specifica il tipo di un oggetto Office Math in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Specifica il tipo di un oggetto Office [Math](../).

```cpp
enum class MathObjectType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| OMath | 0 | Istanza di testo matematico. |
| OMathPara | 1 | Paragrafo [Math](../) o zona di visualizzazione matematica, che contiene uno o più elementi [OMath](./) in modalità di visualizzazione. |
| Accent | 2 | Funzione Accent, composta da una base e un segno diacritico combinante. |
| Barra | 3 | Funzione Bar, composta da un argomento base e una barra superiore o inferiore. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Oggetto Box, composto da un bordo disegnato attorno a un'istanza di testo matematico (come una formula o un'equazione) |
| Box | 5 | Oggetto Box, utilizzato per raggruppare componenti di un'equazione o di un'altra istanza di testo matematico. |
| Delimitatore | 6 | Oggetto delimitatore, costituito da delimitatori di apertura e chiusura (come parentesi tonde, graffe, quadre e barre verticali), e da un elemento contenuto al suo interno. |
| Grado | 7 | Grado nel radicale matematico. |
| Argument | 8 | Oggetto argomento. Racchiude le entità Office [Math](../) quando vengono usate come argomenti per altre entità Office [Math](../). |
| Array | 9 | Oggetto array, costituito da una o più equazioni, espressioni o altri blocchi di testo matematico che possono essere allineati verticalmente come un'unità rispetto al testo circostante sulla riga. |
| Frazione | 10 | Oggetto frazione, costituito da un numeratore e un denominatore separati da una barra di frazione. |
| Denominatore | 11 | Denominatore di un oggetto frazione. |
| Numeratore | 12 | Numeratore dell'oggetto Frazione. |
| Funzione | 13 | Oggetto Funzione-Applica, che consiste in un nome di funzione e in un elemento argomento su cui agire. |
| FunctionName | 14 | Nome della funzione. Per esempio, i nomi delle funzioni sono sin e cos. |
| GroupCharacter | 15 | Oggetto Gruppo-Carattere, costituito da un carattere disegnato sopra o sotto il testo, spesso con lo scopo di raggruppare visivamente gli elementi. |
| Limit | 16 | Limite inferiore dell'oggetto [LowerLimit](./) e limite superiore della funzione [UpperLimit](./). |
| LowerLimit | 17 | Oggetto Limite-Inferiore, costituito da testo sulla linea di base e testo di dimensione ridotta immediatamente al di sotto. |
| UpperLimit | 18 | Oggetto Limite-Superiore, costituito da testo sulla linea di base e testo di dimensione ridotta immediatamente al di sopra. |
| Matrice | 19 | Oggetto matrice, costituito da uno o più elementi disposti in una o più righe e una o più colonne. |
| MatrixRow | 20 | Singola riga della matrice. |
| NAry | 21 | Oggetto n-ario, costituito da un oggetto n-ario, una base (o operando) e limiti superiori e inferiori opzionali. |
| Phantom | 22 | Oggetto fantasma. |
| Radical | 23 | Oggetto radicale, costituito da un radicale, un elemento base e un grado opzionale. |
| SubscriptPart | 24 | Pedice dell'oggetto che può avere una parte di pedice. |
| SuperscriptPart | 25 | Apice dell'oggetto apice. |
| PreSubSuperscript | 26 | Oggetto Pre-Sub-Superscript, che consiste in un elemento base e un pedice e un apice posizionati a sinistra della base. |
| Subscript | 27 | Oggetto pedice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sotto e a destra. |
| SubSuperscript | 28 | Oggetto Sub-superscript, che consiste in un elemento base, uno script di dimensioni ridotte posizionato sotto e a destra, e uno script di dimensioni ridotte posizionato sopra e a destra. |
| Superscript | 29 | Oggetto apice, che consiste in un elemento base e uno script di dimensioni ridotte posizionato sopra e a destra. |
| None | 30 | Il tipo di oggetto non è specificato. |

## Vedi anche

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
