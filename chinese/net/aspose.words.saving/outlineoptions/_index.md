---
title: OutlineOptions Class
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.OutlineOptions 类来自定义文档的大纲设置，以增强组织性和清晰度。
type: docs
weight: 6140
url: /zh/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

允许指定轮廓选项。

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class OutlineOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | 允许指定单个书签的大纲级别。 |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | 获取或设置一个值，该值确定在文档导出时是否创建缺失的轮廓级别。 |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | 指定是否为表格内的标题（用标题样式格式化的段落）创建轮廓。 |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | 指定文档大纲中显示 Word 书签的默认级别。 |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | 指定查看文件时文档大纲中展开显示的级别数。 |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | 指定文档大纲中应包含多少级标题（使用标题样式格式化的段落）。 |

## 例子

显示处理我们正在呈现为 PDF 的文档中的页眉/页脚中的书签。

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“PageMode”属性设置为“PdfPageMode.UseOutlines”以在输出 PDF 中显示大纲导航窗格。
saveOptions.PageMode = PdfPageMode.UseOutlines;

// 将“DefaultBookmarksOutlineLevel”属性设置为“1”以显示所有
// 输出 PDF 中大纲第一级的书签。
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// 将“HeaderFooterBookmarksExportMode”属性设置为“HeaderFooterBookmarksExportMode.None”
// 不导出页眉/页脚内的任何书签。
// 将“HeaderFooterBookmarksExportMode”属性设置为“HeaderFooterBookmarksExportMode.First”
// 仅导出第一部分的页眉/页脚中的书签。
// 将“HeaderFooterBookmarksExportMode”属性设置为“HeaderFooterBookmarksExportMode.All”
// 导出所有页眉/页脚中的书签。
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
