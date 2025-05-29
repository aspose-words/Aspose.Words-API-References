---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words for .NET
description: 探索 StyleCollection DefaultFont 属性，实现无缝文档文本格式设置。以一致、专业的风格提升您的文档质量。
type: docs
weight: 20
url: /zh/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

获取文档默认文本格式。

```csharp
public Font DefaultFont { get; }
```

## 评论

请注意，文档范围的默认值是在 Microsoft Word 2007 中引入的，并且完全受 OOXML 格式支持（Docx) 仅。 早期的文档格式对该功能的支持有限，并且只能存储字体名称。

## 例子

展示如何将样式添加到文档的样式集合中。

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// 为我们稍后可能添加到此集合的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";
// 如果我们添加“StyleType.Paragraph”样式，集合将应用以下值
// 将其“DefaultParagraphFormat”属性设置为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// 添加样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### 也可以看看

* class [Font](../../font/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
