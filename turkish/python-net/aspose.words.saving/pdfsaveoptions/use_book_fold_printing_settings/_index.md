---
title: PdfSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 340
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/use_book_fold_printing_settings/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın, içeriği düzenlemek için
# çıktı PDF'de, onu bir kitapçık yapmak için kullanmamıza yardımcı olacak şekilde.
# PDF'yi normal olarak oluşturmak için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
options.use_book_fold_printing_settings = render_text_as_bookfold
# Belgeyi bir kitapçık olarak oluşturuyorsak, "MultiplePages" özelliğini ayarlamalıyız
# tüm bölümlerin sayfa ayarı nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
if render_text_as_bookfold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Bu belgeyi sayfaların her iki tarafına bastıktan sonra, tüm sayfaları bir anda ortasından katlayabiliriz,
# ve içerikler bir kitapçık oluşturacak şekilde hizalanır.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.SaveAsPdfBookFold.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

