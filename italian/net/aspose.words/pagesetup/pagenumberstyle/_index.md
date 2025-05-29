---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageSetup PageNumberStyle per personalizzare facilmente il formato dei numeri di pagina, migliorando la presentazione e la chiarezza del documento.
type: docs
weight: 320
url: /it/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

Ottiene o imposta il formato del numero di pagina.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

## Esempi

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

// Sposta il generatore di documenti nell'intestazione primaria della prima sezione,
// che verrà visualizzata in ogni pagina di quella sezione.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Inserire un campo PAGINA, che visualizzerà il numero della pagina corrente.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configurare la sezione in modo che il conteggio delle pagine visualizzato nei campi PAGE parta da 5.
// Inoltre, configura tutti i campi PAGE in modo che visualizzino i numeri di pagina utilizzando numeri romani maiuscoli.
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

// Configurare la sezione in modo che il conteggio delle pagine visualizzato nei campi PAGE parta da 10.
// Inoltre, configura tutti i campi PAGE in modo che visualizzino i numeri di pagina utilizzando numeri arabi.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Guarda anche

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
