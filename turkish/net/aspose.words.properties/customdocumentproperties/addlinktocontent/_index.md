---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words for .NET
description: CustomDocumentProperties AddLinkToContent yöntem. İçeriğe bağlı yeni bir özel belge özelliği oluşturur C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

İçeriğe bağlı yeni bir özel belge özelliği oluşturur.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| linkSource | String | Mülkiyetin kaynağı. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi veya`hükümsüz` ne zaman*linkSource* geçersizdir.

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
