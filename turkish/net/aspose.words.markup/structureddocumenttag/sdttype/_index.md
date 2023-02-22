---
title: StructuredDocumentTag.SdtType
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Bunun türünü alır Yapılandırılmış belge etiketi .
type: docs
weight: 250
url: /tr/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Bunun türünü alır **Yapılandırılmış belge etiketi** .

```csharp
public SdtType SdtType { get; }
```

### Örnekler

Yapılandırılmış bir belge etiketinin türünün nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Ayrıca bakınız

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag/)
* toplantı [Aspose.Words](../../../)


