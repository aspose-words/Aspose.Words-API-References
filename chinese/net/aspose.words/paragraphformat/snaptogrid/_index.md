---
title: ParagraphFormat.SnapToGrid
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 指定当前段落在布置段落中的内容时是否应使用文档每页网格线设置 
type: docs
weight: 290
url: /zh/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

指定当前段落在布置段落中的内容时是否应使用文档每页网格线设置 。

```csharp
public bool SnapToGrid { get; set; }
```

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

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


