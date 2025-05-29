---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Saving.HeaderFooterBookmarksExportMode 如何增强页眉和页脚中的书签导出功能，实现无缝文档管理。
type: docs
weight: 5800
url: /zh/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

指定如何导出页眉/页脚中的书签。

```csharp
public enum HeaderFooterBookmarksExportMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 页眉/页脚中的书签未导出。 |
| First | `1` | 仅导出该部分第一个页眉/页脚中的书签。 |
| All | `2` | 所有页眉/页脚中的书签均已导出。 |

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
