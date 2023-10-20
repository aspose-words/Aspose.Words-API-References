---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words per .NET
description: PageSetup OddAndEvenPagesHeaderFooter proprietà. Vero se il documento ha intestazioni e piè di pagina diversi per le pagine con numeri dispari e con numeri pari in C#.
type: docs
weight: 280
url: /it/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Vero se il documento ha intestazioni e piè di pagina diversi per le pagine con numeri dispari e con numeri pari.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Osservazioni

Nota: la modifica di questa proprietà influisce su tutte le sezioni del documento.

## Esempi

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica che vogliamo intestazioni e piè di pagina diversi per le prime pagine, pari e dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ciascun tipo di intestazione.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Mostra come abilitare o disabilitare anche le intestazioni/piè di pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di intestazione/piè di pagina.
// 1 - L'intestazione/piè di pagina "Principale", che appare su ogni pagina della sezione.
 // Possiamo sovrascrivere l'intestazione/piè di pagina principale con un'intestazione/piè di pagina pari e la prima.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - L'intestazione/piè di pagina "Pari", che appare su ogni pagina pari di questa sezione.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Ogni sezione ha un oggetto "PageSetup" che specifica le proprietà relative all'aspetto della pagina
// come orientamento, dimensione e bordi.
// Imposta la proprietà "OddAndEvenPagesHeaderFooter" su "true"
// per visualizzare l'intestazione/piè di pagina pari sulle pagine pari.
// Imposta la proprietà "OddAndEvenPagesHeaderFooter" su "false"
// per visualizzare l'intestazione/piè di pagina principale sulle pagine pari.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
