---
title: StyleCollection.Count
linktitle: Count
articleTitle: Count
second_title: 用于 .NET 的 Aspose.Words
description: StyleCollection Count 财产. 获取集合中的样式数量 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

获取集合中的样式数量。

```csharp
public int Count { get; }
```

## 例子

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

* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
