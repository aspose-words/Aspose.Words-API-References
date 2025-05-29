---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: Aspose.Words for .NET
description: 使用 Style Aliases 属性轻松发现所有样式别名。如果不存在，则返回一个空字符串数组。简化您的样式管理！
type: docs
weight: 10
url: /zh/net/aspose.words/style/aliases/
---
## Style.Aliases property

获取此样式的所有别名。如果样式没有别名，则返回空的字符串数组。

```csharp
public string[] Aliases { get; }
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
