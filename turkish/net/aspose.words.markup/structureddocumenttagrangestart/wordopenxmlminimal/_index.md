---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: .NET için Aspose.Words
description: WordOpenXMLMinimal'deki StructuredDocumentTagRangeStart özelliğini keşfedin. Yalnızca içeriğe odaklanarak FlatOpc biçimindeki basitleştirilmiş bir XML dizesine erişin.
type: docs
weight: 180
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc format. Bunun aksine[`WordOpenXML`](../wordopenxml/) özellik, bu yöntem içerikle ilgili olmayan parçaları hariç tutan soyulmuş bir belge oluşturur.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Örnekler

FlatOpc formatında düğüm içerisinde bulunan en küçük XML'in nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### Ayrıca bakınız

* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
