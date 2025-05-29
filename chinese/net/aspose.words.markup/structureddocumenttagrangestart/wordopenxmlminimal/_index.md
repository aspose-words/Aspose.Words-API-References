---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words for .NET
description: 探索 WordOpenXMLMinimal 中的 StructuredDocumentTagRangeStart 属性。访问 FlatOpc 格式的精简 XML 字符串，仅关注内容。
type: docs
weight: 180
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

获取表示节点中包含的 XML 的字符串FlatOpc格式. 与[`WordOpenXML`](../wordopenxml/)属性，此方法生成一个精简的文档，排除任何与内容无关的部分。

```csharp
public string WordOpenXMLMinimal { get; }
```

## 例子

展示如何获取 FlatOpc 格式的节点中包含的最小 XML。

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### 也可以看看

* class [StructuredDocumentTagRangeStart](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
