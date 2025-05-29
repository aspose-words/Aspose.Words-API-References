---
title: PageSetup.RestartPageNumbering
linktitle: RestartPageNumbering
articleTitle: RestartPageNumbering
second_title: Aspose.Words per .NET
description: Scopri come la proprietà RestartPageNumbering migliora la formattazione dei documenti consentendo la numerazione delle pagine specifica per sezione. Ottimizza il tuo layout senza sforzo!
type: docs
weight: 360
url: /it/net/aspose.words/pagesetup/restartpagenumbering/
---
## PageSetup.RestartPageNumbering property

Vero se la numerazione delle pagine ricomincia dall'inizio della sezione.

```csharp
public bool RestartPageNumbering { get; set; }
```

## Osservazioni

Se impostato su`falso` , IL`RestartPageNumbering` la proprietà sovrascriverà the [`PageStartingNumber`](../pagestartingnumber/) proprietà in modo che la numerazione delle pagine possa continuare dalla sezione precedente.

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

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
