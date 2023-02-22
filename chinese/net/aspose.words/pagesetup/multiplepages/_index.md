---
title: PageSetup.MultiplePages
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 对于多页文档获取或设置文档的打印或渲染方式以便将其装订为小册子
type: docs
weight: 260
url: /zh/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

对于多页文档，获取或设置文档的打印或渲染方式，以便将其装订为小册子。

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

### 例子

显示如何配置可以作为折页打印的文档。

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

// 配置第一节的“PageSetup”属性，以折页的形式打印文档。
// 当我们把这个文件双面打印出来的时候，我们就可以把页面拿来堆叠起来
// 并立即将它们全部折叠到中间。文档的内容将排列成书折。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// 我们只能以 4 的倍数指定张数。
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

显示如何设置装订线边距。

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

// 装订线将空格添加到左侧或右侧页边距，
// 这弥补了书籍中页面的中心折叠侵占页面的布局。
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // 确定我们的页面在页边距内有多少空间用于文本，然后添加一个量来填充页边距。
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// 将“RtlGutter”属性设置为“true”以将装订线放置在更适合从右到左文本的位置。
pageSetup.RtlGutter = true;

// 将“MultiplePages”属性设置为“MultiplePagesType.MirrorMargins”以交替
// 每页页边距的左/右页边位置。
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### 也可以看看

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


