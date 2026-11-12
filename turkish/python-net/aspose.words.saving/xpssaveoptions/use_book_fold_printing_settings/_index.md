---
title: XpsSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 60
url: /tr/python-net/aspose.words.saving/xpssaveoptions/use_book_fold_printing_settings/
---

## XpsSaveOptions.use_book_fold_printing_settings property

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

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

