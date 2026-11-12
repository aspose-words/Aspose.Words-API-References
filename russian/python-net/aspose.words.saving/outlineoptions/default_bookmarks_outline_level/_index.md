---
title: OutlineOptions.default_bookmarks_outline_level property
linktitle: default_bookmarks_outline_level property
articleTitle: default_bookmarks_outline_level property
second_title: Aspose.Words for Python
description: "OutlineOptions.default_bookmarks_outline_level property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /ru/python-net/aspose.words.saving/outlineoptions/default_bookmarks_outline_level/
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
* class [OutlineOptions](../)

