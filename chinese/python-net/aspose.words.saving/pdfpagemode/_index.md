---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 730
url: /zh/python-net/aspose.words.saving/pdfpagemode/
---

## PdfPageMode enumeration

Specifies how the PDF document should be displayed when opened in the PDF reader.


### Members

| Name | Description |
| --- | --- |
| USE_NONE | Neither document outline nor thumbnail images are visible. |
| USE_OUTLINES | Document outline is visible. Note that if there're no outlines in the PDF document then outline navigation pane will not be visible anyway. |
| USE_THUMBS | Thumbnail images are visible. |
| FULL_SCREEN | Full-screen mode, with no menu bar, window controls, or any other window visible. |
| USE_OC | Optional content group panel is visible. |
| USE_ATTACHMENTS | Attachments panel is visible. |

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

