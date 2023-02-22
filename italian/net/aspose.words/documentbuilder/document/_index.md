---
title: DocumentBuilder.Document
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder proprietà. Ottiene o imposta ilDocument oggetto a cui questo oggetto è collegato.
type: docs
weight: 80
url: /it/net/aspose.words/documentbuilder/document/
---
## DocumentBuilder.Document property

Ottiene o imposta il`Document` oggetto a cui questo oggetto è collegato.

```csharp
public Document Document { get; set; }
```

### Esempi

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica le proprietà di impostazione della pagina per la sezione corrente del builder e aggiungi del testo.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Se iniziamo una nuova sezione utilizzando un generatore di documenti,
// erediterà le attuali proprietà di configurazione della pagina del builder.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Possiamo ripristinare le sue proprietà di impostazione della pagina ai valori predefiniti utilizzando il metodo "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Guarda anche

* class [Document](../../document/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


