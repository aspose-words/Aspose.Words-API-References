---
title: OutlineOptions class
linktitle: OutlineOptions class
articleTitle: OutlineOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.OutlineOptions class. Allows to specify outline options"
type: docs
weight: 570
url: /zh/python-net/aspose.words.saving/outlineoptions/
---

## OutlineOptions class

Allows to specify outline options.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [OutlineOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmarks_outline_levels](./bookmarks_outline_levels/) | Allows to specify individual bookmarks outline level. |
| [create_missing_outline_levels](./create_missing_outline_levels/) | Gets or sets a value determining whether or not to create missing outline levels when the document is  exported. |
| [create_outlines_for_headings_in_tables](./create_outlines_for_headings_in_tables/) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [default_bookmarks_outline_level](./default_bookmarks_outline_level/) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [expanded_outline_levels](./expanded_outline_levels/) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [headings_outline_levels](./headings_outline_levels/) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline. |

### Examples

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Bookmarks in headers and footers.docx')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.PdfSaveOptions()
# 将 "PageMode" 属性设置为 "PdfPageMode.UseOutlines"，以在输出的 PDF 中显示大纲导航窗格。
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# 将 "DefaultBookmarksOutlineLevel" 属性设置为 "1"，以显示所有
# 在输出 PDF 的大纲第一层级的书签。
save_options.outline_options.default_bookmarks_outline_level = 1
# 将 "HeaderFooterBookmarksExportMode" 属性设置为 "HeaderFooterBookmarksExportMode.None"，以
# 不导出位于页眉/页脚中的任何书签。
# 将 "HeaderFooterBookmarksExportMode" 属性设置为 "HeaderFooterBookmarksExportMode.First"，以
# 仅导出第一节的页眉/页脚中的书签。
# 将 "HeaderFooterBookmarksExportMode" 属性设置为 "HeaderFooterBookmarksExportMode.All"，以
# 导出所有页眉/页脚中的书签。
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

