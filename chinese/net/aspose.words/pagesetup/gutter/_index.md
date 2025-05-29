---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: Aspose.Words for .NET
description: 调整 PageSetup 装订线设置，优化文档边距，方便装订。使用完美的边距优化布局，获得专业效果。
type: docs
weight: 160
url: /zh/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

获取或设置为文档装订添加到边距的额外空间量。

```csharp
public double Gutter { get; set; }
```

## 例子

展示如何配置可以打印为书本折页的文档。

```csharp
Document doc = new Document();

// 插入跨越 16 页的文本。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// 配置第一节的“PageSetup”属性，以书本折叠的形式打印文档。
// 当我们双面打印此文档时，我们可以将页面堆叠起来
// 然后将它们全部从中间折叠起来。文档内容将排列成书形折叠。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// 我们只能指定 4 的倍数的纸张数量。
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

展示如何设置装订线边距。

```csharp
Document doc = new Document();

// 插入跨越多页的文本。
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// 装订线会在页面左边缘或右边缘添加空白，
// 这弥补了书中页面中心折叠侵占页面布局的问题。
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // 确定页面边距内有多少空间用于文本，然后添加一定量来填充边距。
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// 将“RtlGutter”属性设置为“true”，以将装订线放置在更适合从右到左的文本的位置。
pageSetup.RtlGutter = true;

// 将“MultiplePages”属性设置为“MultiplePagesType.MirrorMargins”以交替
// 每页边距的左/右页边位置。
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
