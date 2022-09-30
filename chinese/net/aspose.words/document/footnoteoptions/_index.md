---
title: FootnoteOptions
second_title: Aspose.Words for .NET API 参考
description: 提供控制本文档中脚注编号和位置的选项
type: docs
weight: 150
url: /zh/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

提供控制本文档中脚注编号和位置的选项。

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### 例子

显示如何选择文档收集和显示脚注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注是一种将引用或旁注附加到文本的方法
// 这不会干扰主体文本的流动。  
// 插入脚注会添加一个小的上标参考符号
// 在我们插入脚注的主体文本处。
// 每个脚注还在页面底部创建一个条目，由一个符号组成
// 与正文中的引用符号匹配。
// 我们传递给文档构建器的“InsertFootnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// 我们可以使用“Position”属性来确定文档将放置其所有脚注的位置。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BottomOfPage”，
// 每个脚注都将显示在包含其引用标记的页面底部。这是默认值。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BeneathText”，
// 每个脚注都将显示在包含其引用标记的页面文本的末尾。
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

显示如何设置文档开始脚注/尾注计数的数字。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是一种将参考或旁注附加到文本的方法
// 这不会干扰主体文本的流动。 
// 插入脚注/尾注会添加一个小的上标参考符号
// 在我们插入脚注/尾注的主体文本处。
// 每个脚注/尾注还创建一个条目，其中包含一个符号
// 与正文中的引用符号匹配。
// 我们传递给文档构建器的“InsertEndnote”方法的参考文本。
// 默认情况下，脚注条目显示在包含
// 它们的参考符号和尾注出现在文档的末尾。
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// 默认情况下，每个脚注和尾注的引用符号是它的索引
// 在所有文档的脚注/尾注中。每个文档都有单独的计数
// 对于脚注和尾注，它们都从 1 开始。
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// 我们可以使用“StartNumber”属性来获取文档
// 以不同的数字开始脚注或尾注。
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

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

显示如何在文档中的某些位置重新开始脚注/尾注编号。

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
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// 默认情况下，每个脚注和尾注的引用符号是它的索引
// 在所有文档的脚注/尾注中。每个文档都有单独的计数
// 用于脚注和尾注，并且不会在任何时候重新开始这些计数。
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// 我们可以使用“RestartRule”属性来让文档重新启动
//脚注/尾注在新的页面或部分计数。
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### 也可以看看

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
