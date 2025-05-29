---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTag WordOpenXML. Получите доступ к данным XML в формате FlatOpc для бесшовной интеграции документов и расширенной функциональности.
type: docs
weight: 300
url: /ru/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат.

```csharp
public string WordOpenXML { get; }
```

## Примеры

Показывает, как получить XML, содержащийся в узле в формате FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
