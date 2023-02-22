---
title: CustomDocumentProperties.AddLinkToContent
second_title: Aspose.Words for .NET API Referansı
description: CustomDocumentProperties yöntem. İçeriğe bağlı yeni bir özel belge özelliği oluşturur.
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
| linkSource | String | Mülkün kaynağı. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi veya linkSource geçersiz olduğunda null.

### Örnekler

Özel bir belge özelliğinin bir yer işaretine nasıl bağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Yeni bir özel özelliği bir yer işaretine bağla. Bu mülkün değeri
// "LinkSource" üyesinde başvurduğu yer işaretinin içeriği olacaktır.
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
* ad alanı [Aspose.Words.Properties](../../customdocumentproperties/)
* toplantı [Aspose.Words](../../../)


