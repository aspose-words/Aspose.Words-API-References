---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words for .NET
description: 探索 PageSetup SheetsPerBooklet 属性，轻松管理小册子页数，增强文档布局和打印效率。
type: docs
weight: 400
url: /zh/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

返回或设置每本小册子所包含的页数。

```csharp
public int SheetsPerBooklet { get; set; }
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

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
