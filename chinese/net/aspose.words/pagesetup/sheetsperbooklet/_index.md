---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup SheetsPerBooklet 财产. 返回或设置要包含在每个小册子中的页数 在 C#.
type: docs
weight: 400
url: /zh/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

返回或设置要包含在每个小册子中的页数。

```csharp
public int SheetsPerBooklet { get; set; }
```

## 例子

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

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
