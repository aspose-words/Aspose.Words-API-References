---
title: OutlineOptions.default_bookmarks_outline_level property
linktitle: default_bookmarks_outline_level property
articleTitle: default_bookmarks_outline_level property
second_title: Aspose.Words for Python
description: "OutlineOptions.default_bookmarks_outline_level property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /zh/python-net/aspose.words.saving/outlineoptions/default_bookmarks_outline_level/
---

## OutlineOptions.default_bookmarks_outline_level property

Specifies the default level in the document outline at which to display Word bookmarks.


```python
@property
def default_bookmarks_outline_level(self) -> int:
    ...

@default_bookmarks_outline_level.setter
def default_bookmarks_outline_level(self, value: int):
    ...

```

### Remarks

Individual bookmarks level could be specified using [OutlineOptions.bookmarks_outline_levels](../bookmarks_outline_levels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline.
Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.




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

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

