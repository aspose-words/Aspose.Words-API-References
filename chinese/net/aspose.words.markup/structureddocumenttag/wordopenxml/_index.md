---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag WordOpenXML 财产. 获取一个字符串该字符串表示包含在FlatOpc格式 在 C#.
type: docs
weight: 300
url: /zh/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

获取一个字符串，该字符串表示包含在FlatOpc格式.

```csharp
public string WordOpenXML { get; }
```

## 例子

显示如何获取包含在 FlatOpc 格式的节点中的 XML。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
