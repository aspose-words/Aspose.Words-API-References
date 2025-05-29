---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words for .NET
description: 探索 Style Equals 方法，用于比较内置样式。了解链接样式和下一段样式，从而增强格式设置和设计效率。
type: docs
weight: 220
url: /zh/net/aspose.words/style/equals/
---
## Style.Equals method

与指定样式进行比较。 仅比较内置样式的样式 Istds。 比较中不包含样式默认值。 以递归方式比较基本样式、链接样式和下一段落样式。

```csharp
public bool Equals(Style style)
```

## 例子

展示如何使用样式别名。

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// 本文档包含一个名为“MyStyle,MyStyle Alias 1,MyStyle Alias 2”的样式。
// 如果样式的名称有多个用逗号分隔的值，则每个子句都是一个单独的别名。
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// 我们可以使用其别名以及名称来引用样式。
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
