---
title: WordOpenXML
second_title: Справочник по API Aspose.Words для .NET
description: Получает строку представляющую XML содержащийся в узле вFlatOpc формат.
type: docs
weight: 300
url: /ru/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат.

```csharp
public string WordOpenXML { get; }
```

### Примеры

Показывает, как получить XML, содержащийся в узле, в формате FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Смотрите также

* class [StructuredDocumentTag](../../structureddocumenttag)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
