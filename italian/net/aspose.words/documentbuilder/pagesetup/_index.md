---
title: DocumentBuilder.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words per .NET
description: Esplora la proprietà PageSetup di DocumentBuilder per accedere alle impostazioni correnti di pagina e sezione, migliorando l'efficienza del layout e della formattazione del documento.
type: docs
weight: 160
url: /it/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Restituisce un oggetto che rappresenta l'impostazione di pagina corrente e le proprietà della sezione.

```csharp
public PageSetup PageSetup { get; }
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

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
