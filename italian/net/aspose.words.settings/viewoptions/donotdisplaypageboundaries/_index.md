---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words per .NET
description: ViewOptions DoNotDisplayPageBoundaries proprietà. Disattiva la visualizzazione dello spazio tra la parte superiore del testo e il bordo superiore della pagina in C#.
type: docs
weight: 20
url: /it/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Disattiva la visualizzazione dello spazio tra la parte superiore del testo e il bordo superiore della pagina.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## Esempi

Mostra come nascondere gli spazi bianchi verticali e le intestazioni/piè di pagina nelle opzioni di visualizzazione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci contenuto che si estende su 3 pagine.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Inserisce un'intestazione e un piè di pagina.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Questo documento contiene una piccola quantità di contenuto che occupa alcune pagine intere di spazio.
// Imposta il flag "DoNotDisplayPageBoundaries" su "true" per fare in modo che le versioni precedenti di Microsoft Word omettano le intestazioni,
// piè di pagina e gran parte dello spazio bianco verticale durante la visualizzazione del nostro documento.
// Imposta il flag "DoNotDisplayPageBoundaries" su "false" per ottenere versioni precedenti di Microsoft Word
// per visualizzare normalmente il nostro documento.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Guarda anche

* class [ViewOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
