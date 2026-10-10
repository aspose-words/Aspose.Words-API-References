---
title: PdfSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 340
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/use_book_fold_printing_settings/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
# i utdata‑PDF på ett sätt som hjälper oss att använda den för att göra en häfte.
# Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera PDF-filen normalt.
options.use_book_fold_printing_settings = render_text_as_bookfold
# Om vi renderar dokumentet som en häfte, måste vi sätta "MultiplePages"
# egenskaperna för sidinställningsobjekten i alla sektioner till "MultiplePagesType.BookFoldPrinting".
if render_text_as_bookfold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# När vi skriver ut detta dokument på båda sidor av sidorna, kan vi vika alla sidor på mitten på en gång,
# och innehållet kommer att stämma överens på ett sätt som skapar ett häfte.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.SaveAsPdfBookFold.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

