---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà Document ViewOptions per personalizzare le impostazioni di visualizzazione di Microsoft Word e ottenere un'esperienza di visualizzazione su misura.
type: docs
weight: 490
url: /it/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Fornisce opzioni per controllare la modalità di visualizzazione del documento in Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
```

## Esempi

Mostra come impostare un fattore di zoom personalizzato che le vecchie versioni di Microsoft Word applicheranno a un documento al momento del caricamento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Mostra come impostare un tipo di zoom personalizzato che le vecchie versioni di Microsoft Word applicheranno a un documento al momento del caricamento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Imposta la proprietà "ZoomType" su "ZoomType.PageWidth" per ottenere Microsoft Word
// per ingrandire automaticamente il documento in modo che si adatti alla larghezza della pagina.
// Imposta la proprietà "ZoomType" su "ZoomType.FullPage" per ottenere Microsoft Word
// per ingrandire automaticamente il documento e rendere visibile l'intera prima pagina.
// Imposta la proprietà "ZoomType" su "ZoomType.TextFit" per ottenere Microsoft Word
// per ingrandire automaticamente il documento in modo che si adatti ai margini interni del testo della prima pagina.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Guarda anche

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
