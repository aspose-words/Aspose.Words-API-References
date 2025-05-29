---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words per .NET
description: Scopri il metodo AddLinkToContent di CustomDocumentProperties per creare senza sforzo proprietà di documenti personalizzati collegati per una migliore gestione dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Crea una nuova proprietà personalizzata del documento collegata al contenuto.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Il nome della proprietà. |
| linkSource | String | L'origine della proprietà. |

### Valore di ritorno

L'oggetto di proprietà appena creato o`null` quando il*linkSource* non è valido.

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
