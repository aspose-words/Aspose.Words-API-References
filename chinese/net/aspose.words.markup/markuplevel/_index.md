---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.MarkupLevel 枚举，定义 StructuredDocumentTags 在文档树中的位置，以增强组织和控制。
type: docs
weight: 4670
url: /zh/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

指定文档树中的特定层级[`StructuredDocumentTag`](../structureddocumenttag/)可能发生。

```csharp
public enum MarkupLevel
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Unknown | `0` | 指定未知或无效的值。 |
| Inline | `1` | 该元素出现在内联级别（例如在文本运行中）。 |
| Block | `2` | 该元素出现在块级别（例如在表格和段落之间）。 |
| Row | `3` | 该元素出现在表中的行之间。 |
| Cell | `4` | 该元素出现在一行中的单元格之间。 |

## 例子

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是将文档中的样式应用到结构化文档标签的两种方法。
// 1 - 从文档的样式集合中应用样式对象：
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - 通过名称引用文档中的样式：
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
