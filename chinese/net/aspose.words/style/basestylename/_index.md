---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: 用于 .NET 的 Aspose.Words
description: Style BaseStyleName 财产. 获取/设置此样式所基于的样式的名称 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

获取/设置此样式所基于的样式的名称。

```csharp
public string BaseStyleName { get; set; }
```

## 评论

如果样式不基于任何其他样式，这将是一个空字符串，并且可以将其设置 为空字符串。

## 例子

展示如何使用样式别名。

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// 此文档包含名为“MyStyle,MyStyle Alias 1,MyStyle Alias 2”的样式。
// 如果样式名称有多个用逗号分隔的值，则每个子句都是一个单独的别名。
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// 我们可以使用它的别名以及它的名称来引用一个样式。
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
