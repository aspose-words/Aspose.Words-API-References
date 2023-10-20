---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag WordOpenXMLMinimal 财产. 获取表示节点中包含的 XML 的字符串FlatOpc格式. 与WordOpenXML属性此方法生成一个精简文档排除任何与内容无关的部分 在 C#.
type: docs
weight: 310
url: /zh/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

获取表示节点中包含的 XML 的字符串FlatOpc格式. 与[`WordOpenXML`](../wordopenxml/)属性，此方法生成一个精简文档，排除任何与内容无关的部分。

```csharp
public string WordOpenXMLMinimal { get; }
```

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

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
