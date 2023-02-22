---
title: EndnoteOptions.NumberStyle
second_title: Aspose.Words for .NET API 参考
description: EndnoteOptions 财产. 指定自动编号尾注的数字格式
type: docs
weight: 10
url: /zh/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

指定自动编号尾注的数字格式。

```csharp
public NumberStyle NumberStyle { get; set; }
```

### 评论

并非所有数字样式都适用于此属性。有关适用的 编号样式列表，请参见 Microsoft Word 中的插入脚注或尾注对话框。如果您选择 一个不适用的数字样式，Microsoft Word 将恢复为默认值。

### 例子

显示如何更改脚注/尾注参考标记的编号样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是一种将参考或旁注附加到文本的方法
// 这不会干扰主体文本的流动。 
// 插入脚注/尾注会添加一个小的上标参考符号
// 在我们插入脚注/尾注的主体文本处。
// 每个脚注/尾注还创建一个条目，其中包含一个与引用匹配的符号
// 主体文本中的符号。我们传递给文档构建器的“InsertEndnote”方法的参考文本。
// 默认情况下，脚注条目显示在包含
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

// 默认情况下，每个脚注和尾注的引用符号是它的索引
// 在所有文档的脚注/尾注中。每个文档都有单独的计数
// 用于脚注和尾注。默认情况下，脚注使用阿拉伯数字显示其编号，
// 和尾注以小写罗马数字显示它们的数字。
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// 我们可以使用“NumberStyle”属性将自定义编号样式应用于脚注和尾注。
// 这不会影响带有自定义参考标记的脚注/尾注。
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### 也可以看看

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../endnoteoptions/)
* 部件 [Aspose.Words](../../../)


