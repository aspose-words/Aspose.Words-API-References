---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用“样式移除”方法，轻松从文档中删除不需要的样式。提升内容外观，并保持一致性！
type: docs
weight: 230
url: /zh/net/aspose.words/style/remove/
---
## Style.Remove method

从文档中删除指定的样式。

```csharp
public void Remove()
```

## 评论

删除样式会对文档模型产生以下影响：

* 所有对该样式的引用均从相应的段落、行和表中删除。
* 如果删除了基本样式，其格式将移至子样式。
* 如果要删除的样式具有链接样式，则将同时删除这两个样式。

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

// 将文档中的一种样式应用到文档构建器正在创建的段落。
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// 从文档的样式集合中删除我们的自定义样式。
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// 任何使用已删除样式的文本都会恢复为默认格式。
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
