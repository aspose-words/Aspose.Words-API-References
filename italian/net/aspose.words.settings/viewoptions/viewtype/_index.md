---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words per .NET
description: Scopri la proprietà ViewType di ViewOptions per personalizzare facilmente la modalità di visualizzazione di Microsoft Word, per una maggiore produttività e un'esperienza di modifica su misura.
type: docs
weight: 40
url: /it/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Controlla la modalità di visualizzazione in Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

## Osservazioni

Sebbene Aspose.Words sia in grado di leggere e scrivere questa opzione, il suo utilizzo è specifico dell'applicazione. Ad esempio, MS Word 2013 non rispetta il valore di questa opzione.

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

### Guarda anche

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
