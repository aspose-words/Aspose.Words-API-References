---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /tr/python-net/aspose.words.saving/xpssaveoptions/__init__/
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
# "XpsSaveOptions" nesnesi oluşturun ve bunu belgenin "Save" metoduna geçirebiliriz
# bu metodun belgeyi .XPS'e nasıl dönüştürdüğünü değiştirmek için.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın, içeriği düzenlemek için
# çıktı XPS'te, bunu bir kitapçık oluşturmak için kullanmamıza yardımcı olacak şekilde.
# "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayarak XPS'i normal şekilde oluşturun.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# Belgeyi bir kitapçık olarak oluşturuyorsak, "MultiplePages" özelliğini ayarlamalıyız
# tüm bölümlerin sayfa ayarı nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Bu belgeyi bir kez yazdırdığımızda, sayfaları üst üste koyarak onu bir kitapçığa dönüştürebiliriz
# yazıcıdan çıktıktan sonra ortasından katlayarak.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

