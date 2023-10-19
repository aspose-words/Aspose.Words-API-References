---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words for .NET
description: DocumentProperty LinkSource mülk. Bağlantılı özel belge özelliğinin kaynağını alır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Bağlantılı özel belge özelliğinin kaynağını alır.

```csharp
public string LinkSource { get; }
```

## Örnekler

Özel bir belge özelliğinin bir yer imine nasıl bağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Yeni bir özel özelliği bir yer imine bağlayın. Bu mülkün değeri
// "LinkSource" üyesinde başvuruda bulunduğu yer iminin içeriği olacaktır.
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Ayrıca bakınız

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
