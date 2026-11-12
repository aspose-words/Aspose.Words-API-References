---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /ru/python-net/aspose.words.saving/xpssaveoptions/__init__/
---

## XpsSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) format.



```python
def __init__(self):
    ...
```

## XpsSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) or [SaveFormat.OPEN_XPS](../../../aspose.words/saveformat/#OPEN_XPS) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to save a document to the XPS format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Создайте объект "XpsSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в .XPS.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# Установите свойство "UseBookFoldPrintingSettings" в "true", чтобы расположить содержимое
# в выходном XPS таким образом, чтобы мы могли использовать его для создания брошюры.
# Установите свойство "UseBookFoldPrintingSettings" в значение "false", чтобы отобразить XPS нормально.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# Если мы рендерим документ в виде брошюры, мы должны установить "MultiplePages"
# свойства объектов настройки страниц всех секций на "MultiplePagesType.BookFoldPrinting".
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# После печати этого документа мы можем превратить его в брошюру, сложив страницы
# выходящие из принтера и сложив их пополам.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

