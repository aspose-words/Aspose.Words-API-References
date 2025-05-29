---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTagRangeStart в WordOpenXMLMinimal. Получите доступ к оптимизированной строке XML в формате FlatOpc, сосредоточившись исключительно на контенте.
type: docs
weight: 180
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат. В отличие от[`WordOpenXML`](../wordopenxml/) свойство, этот метод генерирует урезанный документ, который исключает любые части, не связанные с содержимым.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Примеры

Показывает, как получить минимальный XML, содержащийся в узле в формате FlatOpc.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### Смотрите также

* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
