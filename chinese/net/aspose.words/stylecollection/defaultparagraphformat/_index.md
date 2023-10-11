---
title: StyleCollection.DefaultParagraphFormat
second_title: Aspose.Words for .NET API 参考
description: StyleCollection 财产. 获取文档默认段落格式
type: docs
weight: 30
url: /zh/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

获取文档默认段落格式。

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

### 评论

请注意，文档范围的默认值是在 Microsoft Word 2007 中引入的，并且完全支持 OOXML 格式（Docx) 仅。 早期文档格式不支持文档默认段落格式。

### 例子

演示如何将样式添加到文档的样式集合中。

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// 为我们稍后可能添加到此集合中的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";
// 如果我们添加“StyleType.Paragraph”的样式，集合将应用以下值
// 将其“DefaultParagraphFormat”属性设置为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// 添加样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### 也可以看看

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../stylecollection/)
* 部件 [Aspose.Words](../../../)


