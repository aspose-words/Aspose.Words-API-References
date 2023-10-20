---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Notes.FootnoteOptions 班级. 表示文档或部分的脚注编号选项 在 C#.
type: docs
weight: 4280
url: /zh/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

表示文档或部分的脚注编号选项。

要了解更多信息，请访问[使用脚注和尾注](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/)文档文章。

```csharp
public sealed class FootnoteOptions
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | 指定脚注区域格式化的列数。 |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | 指定自动编号脚注的数字格式。 |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | 指定脚注位置。 |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | 确定自动编号何时重新启动。 |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | 指定第一个自动编号脚注的起始数字或字符。 |

## 例子

演示如何将脚注部分拆分为给定数量的列。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

演示如何选择文档收集和显示脚注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注是一种将引用或旁注附加到文本的方法
// 这不会干扰主体文本的流程。
// 插入脚注会添加一个小上标引用符号
// 在正文文本处插入脚注。
// 每个脚注还在页面底部创建一个条目，由一个符号组成
// 与主体文本中的引用符号相匹配。
// 我们传递给文档构建器的“InsertFootnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// 我们可以使用“Position”属性来确定文档放置所有脚注的位置。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BottomOfPage”，
// 每个脚注都会显示在包含其引用标记的页面底部。这是默认值。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BeneathText”，
// 每个脚注都将显示在包含其引用标记的页面文本的末尾。
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

演示如何设置文档开始脚注/尾注计数的数字。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是一种将参考文献或旁注附加到文本的方法
// 这不会干扰主体文本的流程。
// 插入脚注/尾注会添加一个小上标参考符号
// 在正文文本处插入脚注/尾注。
// 每个脚注/尾注还创建一个条目，其中包含一个符号
// 与主体文本中的引用符号相匹配。
// 我们传递给文档构建器的“InsertEndnote”方法的参考文本。
// 脚注条目默认显示在包含以下内容的每个页面的底部
// 它们的参考符号和尾注显示在文档的末尾。
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

// 默认情况下，每个脚注和尾注的引用符号是其索引
// 在文档的所有脚注/尾注中。每个文档维护单独的计数
// 用于脚注和尾注，两者都从 1 开始。
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// 我们可以使用“StartNumber”属性来获取文档
// 以不同的数字开始脚注或尾注计数。
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

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

显示如何在文档中的某些位置重新开始脚注/尾注编号。

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

// 默认情况下，每个脚注和尾注的引用符号是其索引
// 在文档的所有脚注/尾注中。每个文档维护单独的计数
// 对于脚注和尾注，并且不会在任何时候重新开始计数。
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// 我们可以使用“RestartRule”属性来让文档重新启动
// 脚注/尾注计入新页面或新章节。
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### 也可以看看

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
