---
title: PageSetup.PageStartingNumber
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Ottiene o imposta il numero di pagina iniziale della sezione.
type: docs
weight: 330
url: /it/net/aspose.words/pagesetup/pagestartingnumber/
---
## PageSetup.PageStartingNumber property

Ottiene o imposta il numero di pagina iniziale della sezione.

```csharp
public int PageStartingNumber { get; set; }
```

### Osservazioni

Il[`RestartPageNumbering`](../restartpagenumbering/)proprietà, se impostata su`falso` , sovrascriverà the `PageStartingNumber` proprietà in modo che la numerazione delle pagine possa continuare dalla sezione precedente.

### Esempi

Mostra come impostare la numerazione delle pagine in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Sposta il generatore di documenti sull'intestazione principale della prima sezione,
// che verrà visualizzata in ogni pagina di quella sezione.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Inserisci un campo PAGINA, che visualizzerà il numero della pagina corrente.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configura la sezione in modo che il conteggio delle pagine visualizzate nei campi PAGE inizi da 5.
// Inoltre, configura tutti i campi PAGE per visualizzare i relativi numeri di pagina utilizzando numeri romani maiuscoli.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Crea un'altra intestazione primaria per la seconda sezione, con un altro campo PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configura la sezione in modo che il conteggio delle pagine visualizzate nei campi PAGE inizi da 10.
// Inoltre, configura tutti i campi PAGE per visualizzare i numeri di pagina utilizzando numeri arabi.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


