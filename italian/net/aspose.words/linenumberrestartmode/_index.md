---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.LineNumberRestartMode per controllare il ripristino automatico della numerazione delle righe, migliorando la formattazione e la chiarezza dei documenti.
type: docs
weight: 3880
url: /it/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Determina quando riavviare la numerazione automatica delle righe.

```csharp
public enum LineNumberRestartMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| RestartPage | `0` | La numerazione delle righe ricomincia dall'inizio di ogni pagina. |
| RestartSection | `1` | La numerazione delle righe ricomincia dall'inizio della sezione. |
| Continuous | `2` | La numerazione delle righe è continua rispetto alla sezione precedente. |

## Esempi

Mostra come abilitare la numerazione delle righe per una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo utilizzare l'oggetto PageSetup della sezione per visualizzare i numeri a sinistra delle righe di testo della sezione.
// Questo è lo stesso comportamento di un oggetto List,
// ma copre l'intera sezione e non modifica il testo in alcun modo.
// La nostra sezione ricomincerà la numerazione su ogni nuova pagina da 1 e visualizzerà il numero,
// se è un multiplo di 3, a 50 pt a sinistra della riga.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Il contatore di righe salterà qualsiasi paragrafo il cui flag "SuppressLineNumbers" sia impostato su "true".
// Questo paragrafo si trova sulla quindicesima riga, che è un multiplo di 3, e quindi normalmente visualizzerebbe un numero di riga.
// Il contatore di righe della sezione ignorerà anche questa riga, trattando la riga successiva come la quindicesima,
// e continua il conteggio da quel punto in poi.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Guarda anche

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
