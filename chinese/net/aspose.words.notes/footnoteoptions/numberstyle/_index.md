---
title: FootnoteOptions.NumberStyle
second_title: Aspose.Words for .NET API 参考
description: FootnoteOptions 财产. 指定自动编号脚注的数字格式
type: docs
weight: 20
url: /zh/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

指定自动编号脚注的数字格式。

```csharp
public NumberStyle NumberStyle { get; set; }
```

### 评论

并非所有数字样式都适用于该属性。有关适用的 数字样式的列表，请参阅 Microsoft Word 中的“插入脚注”或“尾注”对话框。如果您选择 不适用的数字样式，Microsoft Word 将恢复为默认值。

### 例子

演示如何更改脚注/尾注引用标记的编号样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是一种将参考文献或旁注附加到文本的方法
// 这不会干扰主体文本的流程。
// 插入脚注/尾注会添加一个小上标参考符号
// 在正文文本处插入脚注/尾注。
// 每个脚注/尾注还创建一个条目，其中包含与引用匹配的符号
// 正文中的符号。我们传递给文档生成器的“InsertEndnote”方法的参考文本。
// 脚注条目默认显示在包含以下内容的每个页面的底部
// 它们的参考符号和尾注显示在文档的末尾。
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

// 默认情况下，每个脚注和尾注的引用符号是其索引
// 在文档的所有脚注/尾注中。每个文档维护单独的计数
// 用于脚注和尾注。默认情况下，脚注使用阿拉伯数字显示其编号，
// 和尾注以小写罗马数字显示其编号。
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
* 命名空间 [Aspose.Words.Notes](../../footnoteoptions/)
* 部件 [Aspose.Words](../../../)


