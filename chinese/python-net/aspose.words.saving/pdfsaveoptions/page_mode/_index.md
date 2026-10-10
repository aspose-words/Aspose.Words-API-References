---
title: PdfSaveOptions.page_mode property
linktitle: page_mode property
articleTitle: page_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_mode property. Specifies how the PDF document should be displayed when opened in a PDF reader."
type: docs
weight: 280
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/page_mode/
---

## PdfSaveOptions.page_mode property

Specifies how the PDF document should be displayed when opened in a PDF reader.


```python
@property
def page_mode(self) -> aspose.words.saving.PdfPageMode:
    ...

@page_mode.setter
def page_mode(self, value: aspose.words.saving.PdfPageMode):
    ...

```

### Remarks

The default value is [PdfPageMode.USE_OUTLINES](../../pdfpagemode/#USE_OUTLINES).



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
* class [PdfSaveOptions](../)

