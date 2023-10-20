---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertStyleSeparator 方法. 在文档中插入样式分隔符 在 C#.
type: docs
weight: 450
url: /zh/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

在文档中插入样式分隔符。

```csharp
public void InsertStyleSeparator()
```

## 评论

此方法允许将不同的段落样式应用于文本行的两个不同部分。

## 例子

展示如何使用样式分隔符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 每个段落只能有一种样式。
// InsertStyleSeparator 方法允许我们绕过这个限制。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// 调用 InsertStyleSeparator 方法创建另一个段落，
// 它可以有与以前不同的样式。段落之间不会有中断。
// 输出文档中的文本看起来像一个有两种样式的段落。
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
