---
title: Style.AutomaticallyUpdate
second_title: Aspose.Words for .NET API 参考
description: Style 财产. 指定是否根据适当的值自动重新定义此样式
type: docs
weight: 20
url: /zh/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

指定是否根据适当的值自动重新定义此样式。

```csharp
public bool AutomaticallyUpdate { get; set; }
```

### 评论

如果该属性值设置为 true，则当 适当的段落格式已更改时，MS Word 会自动重新定义当前样式。

自动更新属性仅适用于段落样式。

默认值为`错误的`。

### 例子

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
* 命名空间 [Aspose.Words](../../style/)
* 部件 [Aspose.Words](../../../)


