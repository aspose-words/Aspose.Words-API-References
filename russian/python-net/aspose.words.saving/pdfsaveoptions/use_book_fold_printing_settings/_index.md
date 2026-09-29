---
title: PdfSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 340
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/use_book_fold_printing_settings/
---

## PdfSaveOptions.use_book_fold_printing_settings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout,
if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/).



```python
@property
def use_book_fold_printing_settings(self) -> bool:
    ...

@use_book_fold_printing_settings.setter
def use_book_fold_printing_settings(self, value: bool):
    ...

```

### Remarks

If this option is specified, [FixedPageSaveOptions.page_set](../../fixedpagesaveoptions/page_set/) is ignored when saving.
This behavior matches MS Word.
If book fold printing settings are not specified in page setup, this option will have no effect.





### Examples

Shows how to save a document to the PDF format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "UseBookFoldPrintingSettings" в "true", чтобы расположить содержимое
# в выходном PDF таким образом, чтобы мы могли использовать его для создания буклета.
# Установите свойство "UseBookFoldPrintingSettings" в значение "false", чтобы отобразить PDF нормально.
options.use_book_fold_printing_settings = render_text_as_bookfold
# Если мы рендерим документ в виде брошюры, мы должны установить "MultiplePages"
# свойства объектов настройки страниц всех секций на "MultiplePagesType.BookFoldPrinting".
if render_text_as_bookfold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# После того как мы распечатаем этот документ с обеих сторон страниц, мы можем сложить все страницы пополам одновременно,
# и содержимое выровняется таким образом, что получится брошюра.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.SaveAsPdfBookFold.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

