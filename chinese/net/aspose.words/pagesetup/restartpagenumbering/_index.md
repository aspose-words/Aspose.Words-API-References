---
title: PageSetup.RestartPageNumbering
linktitle: RestartPageNumbering
articleTitle: RestartPageNumbering
second_title: Aspose.Words for .NET
description: 了解 RestartPageNumbering 属性如何通过允许按节指定页码来增强文档格式。轻松优化您的布局！
type: docs
weight: 360
url: /zh/net/aspose.words/pagesetup/restartpagenumbering/
---
## PageSetup.RestartPageNumbering property

如果页码从节的开头重新开始，则为真。

```csharp
public bool RestartPageNumbering { get; set; }
```

## 评论

如果设置为`错误的`， 这`RestartPageNumbering`属性将覆盖 the [`PageStartingNumber`](../pagestartingnumber/)属性，以便页码可以从上一节继续。

## 例子

显示如何在某一部分设置页码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// 将文档构建器移动到第一部分的主标题，
// 该部分中的每个页面都将显示。
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// 插入一个 PAGE 字段，它将显示当前页码。
builder.Write("Page ");
builder.InsertField("PAGE", "");

// 配置该部分以使 PAGE 字段显示的页数从 5 开始。
// 另外，配置所有 PAGE 字段以使用大写罗马数字显示其页码。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// 为第二部分创建另一个主标题，并使用另一个 PAGE 字段。
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// 配置该部分以使 PAGE 字段显示的页数从 10 开始。
// 另外，配置所有 PAGE 字段以使用阿拉伯数字显示其页码。
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
