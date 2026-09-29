---
title: PdfSaveOptions.header_footer_bookmarks_export_mode property
linktitle: header_footer_bookmarks_export_mode property
articleTitle: header_footer_bookmarks_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.header_footer_bookmarks_export_mode property. Determines how bookmarks in headers/footers are exported."
type: docs
weight: 200
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/header_footer_bookmarks_export_mode/
---

## PdfSaveOptions.header_footer_bookmarks_export_mode property

Determines how bookmarks in headers/footers are exported.


```python
@property
def header_footer_bookmarks_export_mode(self) -> aspose.words.saving.HeaderFooterBookmarksExportMode:
    ...

@header_footer_bookmarks_export_mode.setter
def header_footer_bookmarks_export_mode(self, value: aspose.words.saving.HeaderFooterBookmarksExportMode):
    ...

```

### Remarks

The default value is [HeaderFooterBookmarksExportMode.ALL](../../headerfooterbookmarksexportmode/#ALL).

This property is used in conjunction with the [PdfSaveOptions.outline_options](../outline_options/) option.




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

