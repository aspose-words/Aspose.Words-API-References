---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: 用于 .NET 的 Aspose.Words
description: Style Remove 方法. 从文档中删除指定的样式 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words/style/remove/
---
## Style.Remove method

从文档中删除指定的样式。

```csharp
public void Remove()
```

## 评论

样式删除对文档模型有以下影响：

* 所有对该样式的引用都将从相应的段落、运行和表格中删除。
* 如果删除基本样式，其格式将移至子样式。
* 如果要删除的样式具有链接样式，则这两个样式都会被删除。

## 例子

展示如何创建和应用自定义样式。

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// 自动重新定义样式。
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// 将文档中的一种样式应用到文档生成器正在创建的段落。
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// 从文档的样式集合中删除我们的自定义样式。
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// 使用已删除样式的任何文本都会恢复为默认格式。
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
