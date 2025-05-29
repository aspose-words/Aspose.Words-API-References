---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words for .NET
description: 了解如何设置 LinkedStyleName 属性的样式、轻松管理链接样式以及通过无缝集成增强您的设计工作流程。
type: docs
weight: 90
url: /zh/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

获取/设置[`Style`](../)链接到此样式。如果没有链接样式，则返回空字符串。

```csharp
public string LinkedStyleName { get; set; }
```

## 评论

只允许将段落样式链接到字符样式，反之亦然。

为当前样式设置 LinkedStyleName 将自动导致为链接样式设置 LinkedStyleName。

分配空字符串相当于取消先前链接的样式。

## 例子

展示如何将样式相互关联。

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

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
