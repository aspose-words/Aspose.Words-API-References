---
title: PageSetup.LineNumberRestartMode
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words per .NET
description: PageSetup LineNumberRestartMode proprietà. Ottiene o imposta il modo in cui viene eseguita la numerazione delle righe ovvero se ricomincia dallinizio di una nuova pagina o sezione o se viene eseguita in modo continuo in C#.
type: docs
weight: 230
url: /it/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Ottiene o imposta il modo in cui viene eseguita la numerazione delle righe, ovvero se ricomincia dall'inizio di una nuova pagina o sezione o se viene eseguita in modo continuo.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

## Esempi

Mostra come abilitare la numerazione delle righe per una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo utilizzare l'oggetto PageSetup della sezione per visualizzare i numeri a sinistra delle righe di testo della sezione.
// Questo è lo stesso comportamento di un oggetto List,
// ma copre l'intera sezione e non modifica in alcun modo il testo.
// La nostra sezione ricomincerà la numerazione su ogni nuova pagina da 1 e visualizzerà il numero,
// se è un multiplo di 3, a 50pt a sinistra della riga.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Il contatore di riga salterà qualsiasi paragrafo con il flag "SuppressLineNumbers" impostato su "true".
// Questo paragrafo si trova sulla quindicesima riga, che è un multiplo di 3, e quindi normalmente visualizzerebbe un numero di riga.
// Anche il contatore di riga della sezione ignorerà questa riga, tratterà la riga successiva come la quindicesima,
// e continua il conteggio da quel punto in poi.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Guarda anche

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
