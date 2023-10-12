---
title: PageSetup.SheetsPerBooklet
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 返回或设置每本小册子中要包含的页数
type: docs
weight: 400
url: /zh/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

返回或设置每本小册子中要包含的页数。

```csharp
public int SheetsPerBooklet { get; set; }
```

### 例子

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

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


