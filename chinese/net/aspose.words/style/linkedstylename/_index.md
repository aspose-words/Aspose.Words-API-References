---
title: Style.LinkedStyleName
second_title: Aspose.Words for .NET API 参考
description: Style 财产. 获取名称Style与此相关如果没有链接样式则返回空字符串
type: docs
weight: 90
url: /zh/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

获取名称[`Style`](../)与此相关。如果没有链接样式，则返回空字符串。

```csharp
public string LinkedStyleName { get; }
```

### 例子

展示如何使用样式别名。

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// 该文档包含名为“MyStyle,MyStyle Alias 1,MyStyle Alias 2”的样式。
// 如果样式名称具有多个以逗号分隔的值，则每个子句都是一个单独的别名。
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// 我们可以使用其别名及其名称来引用样式。
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
* 命名空间 [Aspose.Words](../../style/)
* 部件 [Aspose.Words](../../../)


