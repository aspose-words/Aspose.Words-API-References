---
title: PageSetup.PageStartingNumber
linktitle: PageStartingNumber
articleTitle: PageStartingNumber
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup PageStartingNumber 财产. 获取或设置section的起始页码 在 C#.
type: docs
weight: 330
url: /zh/net/aspose.words/pagesetup/pagestartingnumber/
---
## PageSetup.PageStartingNumber property

获取或设置section的起始页码

```csharp
public int PageStartingNumber { get; set; }
```

## 评论

的[`RestartPageNumbering`](../restartpagenumbering/)属性，如果设置为**错误的** 将覆盖 the **起始页码**属性，以便页码可以从上一节继续。

## 例子

显示如何在部分中设置页码。

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

// 插入一个 PAGE 字段，它将显示当前页的编号。
builder.Write("Page ");
builder.InsertField("PAGE", "");

// 配置部分以使 PAGE 字段显示的页数从 5 开始。
// 另外，将所有 PAGE 字段配置为使用大写罗马数字显示其页码。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// 为第二个部分创建另一个主标题，带有另一个 PAGE 字段。
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// 将部分配置为使 PAGE 字段显示的页数从 10 开始。
// 另外，将所有 PAGE 字段配置为使用阿拉伯数字显示其页码。
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
