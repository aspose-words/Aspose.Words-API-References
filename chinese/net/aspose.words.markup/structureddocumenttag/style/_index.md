---
title: StructuredDocumentTag.Style
linktitle: Style
articleTitle: Style
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag Style 财产. 获取或设置结构化文档标签的样式 在 C#.
type: docs
weight: 260
url: /zh/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

获取或设置结构化文档标签的样式。

```csharp
public Style Style { get; set; }
```

## 评论

仅 Character风格或Paragraph可以设置链接字符样式的样式。

## 例子

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是将文档样式应用到结构化文档标签的两种方法。
// 1 - 从文档的样式集合中应用样式对象：
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

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### 也可以看看

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
