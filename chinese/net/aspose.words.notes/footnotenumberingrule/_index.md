---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Notes.FootnoteNumberingRule 枚举. 确定何时重新启动自动脚注或尾注编号 在 C#.
type: docs
weight: 4270
url: /zh/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

确定何时重新启动自动脚注或尾注编号。

```csharp
public enum FootnoteNumberingRule
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Continuous | `0` | 在整个文档中连续编号。 |
| RestartSection | `1` | 每个部分重新编号。 |
| RestartPage | `2` | 每页重新编号。仅对脚注有效。 |
| Default | `0` | 等于Continuous. |

## 例子

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

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
