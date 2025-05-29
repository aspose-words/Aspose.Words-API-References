---
title: PageSetup.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Ripristina facilmente l'impostazione di pagina del tuo documento con il metodo ClearFormatting. Ripristina margini, formato carta e orientamento predefiniti per un aspetto impeccabile.
type: docs
weight: 460
url: /it/net/aspose.words/pagesetup/clearformatting/
---
## PageSetup.ClearFormatting method

Ripristina le impostazioni di pagina predefinite per formato carta, margini e orientamento.

```csharp
public void ClearFormatting()
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

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
