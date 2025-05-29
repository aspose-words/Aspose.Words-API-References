---
title: PageSetup.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words per .NET
description: Scopri come la proprietà VerticalAlignment di PageSetup migliora il layout del documento regolando l'allineamento del testo per migliorarne la leggibilità e la presentazione.
type: docs
weight: 450
url: /it/net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

Restituisce o imposta l'allineamento verticale del testo su ogni pagina di un documento o di una sezione.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

## Esempi

Mostra come applicare e ripristinare le impostazioni di impostazione della pagina alle sezioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica le proprietà di impostazione della pagina per la sezione corrente del builder e aggiungi del testo.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Se iniziamo una nuova sezione utilizzando un generatore di documenti,
// erediterà le proprietà di impostazione della pagina corrente del builder.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Possiamo ripristinare i valori predefiniti delle proprietà di impostazione della pagina utilizzando il metodo "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Guarda anche

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
