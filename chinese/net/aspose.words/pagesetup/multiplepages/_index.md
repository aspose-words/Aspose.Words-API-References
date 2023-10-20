---
title: PageSetup.MultiplePages
linktitle: MultiplePages
articleTitle: MultiplePages
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup MultiplePages 财产. 对于多页文档获取或设置文档的打印或呈现方式以便将其装订为小册子 在 C#.
type: docs
weight: 270
url: /zh/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

对于多页文档，获取或设置文档的打印或呈现方式，以便将其装订为小册子。

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

## 例子

演示如何配置可打印为书本折叠的文档。

```csharp
Document doc = new Document();

// 插入跨 16 页的文本。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// 配置第一部分的“PageSetup”属性以书本折叠的形式打印文档。
// 当我们双面打印这个文档时，我们可以把页面叠起来
// 然后将它们全部从中间折叠起来。文档的内容将排列成书本折叠。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// 我们只能指定 4 的倍数的页数。
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

展示如何设置装订线边距。

```csharp
Document doc = new Document();

// 插入跨多页的文本。
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// 装订线在左页边距或右页边距中添加空格，
// 这弥补了书中页面居中折叠侵占页面布局的情况。
PageSetup pageSetup = doc.Sections[0].PageSetup;

// 确定页面的边距内有多少文本空间，然后添加一定量来填充边距。
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// 将“RtlGutter”属性设置为“true”，将装订线放置在更适合从右到左文本的位置。
pageSetup.RtlGutter = true;

// 将“MultiplePages”属性设置为“MultiplePagesType.MirrorMargins”以交替
// 每页边距的左/右页边位置。
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### 也可以看看

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
