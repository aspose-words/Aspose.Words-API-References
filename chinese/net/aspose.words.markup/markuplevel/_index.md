---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Markup.MarkupLevel 枚举. 指定文档树中的特定级别StructuredDocumentTag可能发生 在 C#.
type: docs
weight: 3980
url: /zh/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

指定文档树中的特定级别[`StructuredDocumentTag`](../structureddocumenttag/)可能发生。

```csharp
public enum MarkupLevel
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Unknown | `0` | 指定未知或无效值。 |
| Inline | `1` | 元素出现在内联级别（例如，作为文本运行）。 |
| Block | `2` | 元素出现在块级（例如在表格和段落之间）。 |
| Row | `3` | 元素出现在表中的行之间。 |
| Cell | `4` | 元素出现在一行的单元格中。 |

## 例子

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是将文档中的样式应用到结构化文档标签的两种方法。
// 1 - 应用文档样式集合中的样式对象：
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - 按名称引用文档中的样式：
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
