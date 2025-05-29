---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: .NET için Aspose.Words
description: StructuredDocumentTag WordOpenXML özelliğini keşfedin. Sorunsuz belge entegrasyonu ve gelişmiş işlevsellik için FlatOpc biçimindeki XML verilerine erişin.
type: docs
weight: 300
url: /tr/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc biçim.

```csharp
public string WordOpenXML { get; }
```

## Örnekler

FlatOpc formatında düğüm içerisinde bulunan XML'in nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
