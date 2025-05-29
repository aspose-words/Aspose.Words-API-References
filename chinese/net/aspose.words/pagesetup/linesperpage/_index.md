---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words for .NET
description: 使用 PageSetup LinesPerPage 属性控制文档布局。轻松调整每页行数，以获得最佳的可读性和组织性。
type: docs
weight: 240
url: /zh/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

获取或设置文档网格中每页的行数。

```csharp
public int LinesPerPage { get; set; }
```

## 评论

该属性的最小值为 1。最大值取决于 Normal 样式的页面高度和字体大小。最小行距为字体大小的 136%。例如，对于边距为 1 英寸的 Letter 页面，每页的最大行数为 39。

默认情况下，该属性具有一个值，即行距是 Normal 样式字体大小的 1.5 倍。

## 例子

展示如何指定每页行数的限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后使用它来设置本节每页的行数。
// 足够大的字体大小会将一些行推到下一页以避免字符重叠。
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
