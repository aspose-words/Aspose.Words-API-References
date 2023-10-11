---
title: OutlineOptions.DefaultBookmarksOutlineLevel
second_title: Aspose.Words for .NET API 参考
description: OutlineOptions 财产. 指定文档大纲中显示 Word 书签的默认级别
type: docs
weight: 50
url: /zh/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

指定文档大纲中显示 Word 书签的默认级别。

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

### 评论

可以使用指定单独的书签级别[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/)财产。

指定 0，Word 书签将不会显示在文档大纲中。 指定 1，Word 书签将显示在文档大纲中的第 1 级； 2 表示级别 2，依此类推。

默认值为 0。有效范围为 0 到 9。

### 例子

演示如何处理我们正在渲染为 PDF 的文档中页眉/页脚中的书签。

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“PageMode”属性设置为“PdfPageMode.UseOutlines”以在输出 PDF 中显示大纲导航窗格。
saveOptions.PageMode = PdfPageMode.UseOutlines;

// 将“DefaultBookmarksOutlineLevel”属性设置为“1”以显示所有
// 输出 PDF 中大纲第一层的书签。
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// 将“HeaderFooterBookmarksExportMode”属性设置为“HeaderFooterBookmarksExportMode.None”
// 不导出页眉/页脚内的任何书签。
// 将“HeaderFooterBookmarksExportMode”属性设置为“HeaderFooterBookmarksExportMode.First”
// 仅导出第一部分页眉/页脚中的书签。
// 将“HeaderFooterBookmarksExportMode”属性设置为“HeaderFooterBookmarksExportMode.All”
// 导出所有页眉/页脚中的书签。
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### 也可以看看

* class [OutlineOptions](../)
* 命名空间 [Aspose.Words.Saving](../../outlineoptions/)
* 部件 [Aspose.Words](../../../)


