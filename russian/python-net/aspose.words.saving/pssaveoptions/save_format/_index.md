---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /ru/python-net/aspose.words.saving/pssaveoptions/save_format/
---

## PsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.PS](../../../aspose.words/saveformat/#PS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to the Postscript format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Создайте объект "PsSaveOptions", который мы можем передать в метод "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в PostScript.
# Установите свойство "UseBookFoldPrintingSettings" в "true", чтобы расположить содержимое
# в выходном документе PostScript таким образом, чтобы облегчить создание брошюры.
# Установите свойство "UseBookFoldPrintingSettings" в "false", чтобы сохранять документ обычным способом.
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# Если мы рендерим документ в виде брошюры, мы должны установить "MultiplePages"
# свойства объектов настройки страниц всех секций на "MultiplePagesType.BookFoldPrinting".
for s in doc.sections:
    s = s.as_section()
    s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# После того как мы распечатаем этот документ с обеих сторон страниц, мы можем сложить все страницы пополам одновременно,
# и содержимое выровняется таким образом, что получится брошюра.
doc.save(file_name=ARTIFACTS_DIR + 'PsSaveOptions.UseBookFoldPrintingSettings.ps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

