---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: 用于 .NET 的 Aspose.Words
description: ViewOptions DoNotDisplayPageBoundaries 财产. 关闭文本顶部和页面上边缘之间的空间显示 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

关闭文本顶部和页面上边缘之间的空间显示。

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## 例子

展示如何在视图选项中隐藏垂直空白和页眉/页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入跨 3 页的内容。
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// 插入页眉和页脚。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// 本文档包含少量内容，占用了几整页的空间。
// 将“DoNotDisplayPageBoundaries”标志设置为“true”以使旧版本的 Microsoft Word 省略标题，
// 页脚，以及显示文档时的大部分垂直空白。
// 将“DoNotDisplayPageBoundaries”标志设置为“false”以获取旧版本的 Microsoft Word
// 正常显示我们的文档。
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### 也可以看看

* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
