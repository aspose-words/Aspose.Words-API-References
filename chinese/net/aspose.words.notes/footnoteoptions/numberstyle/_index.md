---
title: FootnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words for .NET
description: 发现 FootnoteOptions NumberStyle 属性，轻松自定义脚注编号格式，以增强文档的清晰度和专业性。
type: docs
weight: 20
url: /zh/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

指定自动编号脚注的数字格式。

```csharp
public NumberStyle NumberStyle { get; set; }
```

## 评论

并非所有数字样式都适用于此属性。有关适用数字样式的列表，请参阅 Microsoft Word 中的“插入脚注或尾注”对话框。如果您选择不适用的数字样式，Microsoft Word 将恢复为默认值。

## 例子

展示如何更改脚注/尾注引用标记的数字样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是将参考或旁注附加到文本的一种方式
// 不会干扰正文的流程。
// 插入脚注/尾注会添加一个小上标引用符号
// 在主体文本中插入脚注/尾注。
// 每个脚注/尾注也会创建一个条目，该条目由与参考匹配的符号组成
// 正文中的符号。我们传递给文档构建器的“InsertEndnote”方法的参考文本。
// 默认情况下，脚注条目显示在包含以下内容的每个页面的底部
// 它们的参考符号和尾注出现在文档的末尾。
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// 默认情况下，每个脚注和尾注的参考符号是其索引
// 在所有文档的脚注/尾注中。每个文档都维护单独的计数
// 用于脚注和尾注。默认情况下，脚注使用阿拉伯数字显示其编号，
// 并且尾注以小写罗马数字显示其编号。
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// 我们可以使用“NumberStyle”属性将自定义编号样式应用于脚注和尾注。
// 这不会影响带有自定义引用标记的脚注/尾注。
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### 也可以看看

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
