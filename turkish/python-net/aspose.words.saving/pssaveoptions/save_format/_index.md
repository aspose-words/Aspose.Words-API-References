---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /tr/python-net/aspose.words.saving/pssaveoptions/save_format/
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
# "PsSaveOptions" nesnesi oluşturun ve belge'nin "Save" yöntemine geçirebiliriz
# bu yöntemin belgeyi PostScript'e nasıl dönüştürdüğünü değiştirmek için.
# "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın, içeriği düzenlemek için
# çıktı Postscript belgesinde, bir kitapçık oluşturmayı kolaylaştıracak şekilde.
# "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın, belgeyi normal şekilde kaydetmek için.
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# Belgeyi bir kitapçık olarak oluşturuyorsak, "MultiplePages" özelliğini ayarlamalıyız
# tüm bölümlerin sayfa ayarı nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
for s in doc.sections:
    s = s.as_section()
    s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Bu belgeyi sayfaların her iki tarafına bastıktan sonra, tüm sayfaları bir anda ortasından katlayabiliriz,
# ve içerikler bir kitapçık oluşturacak şekilde hizalanır.
doc.save(file_name=ARTIFACTS_DIR + 'PsSaveOptions.UseBookFoldPrintingSettings.ps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

