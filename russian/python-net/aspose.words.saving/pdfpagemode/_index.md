---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 730
url: /ru/python-net/aspose.words.saving/pdfpagemode/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
save_options = aw.saving.PdfSaveOptions()
# Установите свойство "PageMode" в "PdfPageMode.UseOutlines", чтобы отобразить панель навигации по структуре в результирующем PDF.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Установите свойство "DefaultBookmarksOutlineLevel" в "1", чтобы отобразить все
# закладки на первом уровне структуры в результирующем PDF.
save_options.outline_options.default_bookmarks_outline_level = 1
# Установите свойство "HeaderFooterBookmarksExportMode" в "HeaderFooterBookmarksExportMode.None", чтобы
# не экспортировать любые закладки, находящиеся в верхних/нижних колонтитулах.
# Установите свойство "HeaderFooterBookmarksExportMode" в "HeaderFooterBookmarksExportMode.First", чтобы
# экспортировать только закладки в верхних/нижних колонтитулах первого раздела.
# Установите свойство "HeaderFooterBookmarksExportMode" в "HeaderFooterBookmarksExportMode.All", чтобы
# экспортировать закладки, находящиеся во всех верхних/нижних колонтитулах.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

