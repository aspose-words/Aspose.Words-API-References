---
title: PageSetup.LinesPerPage
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 获取或设置文档网格中每页的行数
type: docs
weight: 240
url: /zh/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

获取或设置文档网格中每页的行数。

```csharp
public int LinesPerPage { get; set; }
```

### 评论

该属性的最小值为 1。最大值取决于页面高度和 Normal 样式的字体大小。最小行距为字体大小的 136%。例如，页边距为 1 英寸的 Letter 页面的每页最大行数为 39 行。

默认情况下，该属性有一个值，该值的行间距是正常样式的 字体大小的1.5倍。

### 例子

演示如何指定每页可以拥有的行数限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后用它来设置此部分中每页的行数。
// 足够大的字体大小会将某些行向下推到下一页，以避免字符重叠。
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


