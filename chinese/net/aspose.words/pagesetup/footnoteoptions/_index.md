---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup FootnoteOptions 财产. 提供控制本节中脚注的编号和位置的选项 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

提供控制本节中脚注的编号和位置的选项。

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## 例子

展示如何配置影响节中脚注/尾注的选项。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// 配置第一节的所有脚注从1重新开始编号
// 在每个新页面上，并将其直接显示在每个页面上的文本下方。
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// 配置第一部分中的所有尾注以在整个部分中保持连续计数，
// 从 1 开始。此外，将它们全部设置为在文档末尾显示为收集的形式。
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### 也可以看看

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
