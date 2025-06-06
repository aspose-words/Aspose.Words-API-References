---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words per .NET
description: Regola la proprietà ZoomPercent di ViewOptions per impostare il livello di zoom del documento tra il 10 e il 500%. Migliora la leggibilità e ottimizza la tua esperienza di visualizzazione!
type: docs
weight: 50
url: /it/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Ottiene o imposta la percentuale alla quale si desidera visualizzare il documento.

```csharp
public int ZoomPercent { get; set; }
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

* class [ViewOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
