---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: 用于 .NET 的 Aspose.Words
description: StyleCollection DefaultParagraphFormat 财产. 获取文档默认段落格式 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

获取文档默认段落格式。

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## 评论

请注意，Microsoft Word 2007 中引入了文档范围的默认值，并且完全支持 OOXML 格式（Docx) only. 早期的文档格式不支持文档默认段落格式。

## 例子

演示如何将样式添加到文档的样式集合。

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// 为我们稍后可能添加到此集合中的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";

// 如果我们添加“StyleType.Paragraph”的样式，该集合将应用
// 将其“DefaultParagraphFormat”属性转换为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// 添加一个样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### 也可以看看

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
