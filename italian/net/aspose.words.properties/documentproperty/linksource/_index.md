---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words per .NET
description: Scopri la proprietà LinkSource per DocumentProperty, accedi senza sforzo alla fonte delle proprietà personalizzate dei tuoi documenti collegati per una migliore gestione dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Ottiene la fonte di una proprietà di documento personalizzata collegata.

```csharp
public string LinkSource { get; }
```

## Esempi

Mostra come collegare una proprietà personalizzata del documento a un segnalibro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Collega una nuova proprietà personalizzata a un segnalibro. Il valore di questa proprietà
// sarà il contenuto del segnalibro a cui fa riferimento nel membro "LinkSource".
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Guarda anche

* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
