---
title: PdfSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 310
url: /python-net/aspose.words.saving/pdfsaveoptions/use_book_fold_printing_settings/
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
doc = aw.Document(MY_DIR + 'Paragraphs.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "use_book_fold_printing_settings" property to "True" to arrange the contents
# in the output PDF in a way that helps us use it to make a booklet.
# Set the "use_book_fold_printing_settings" property to "False" to render the PDF normally.
options.use_book_fold_printing_settings = render_text_as_bookfold
# If we are rendering the document as a booklet, we must set the "multiple_pages"
# properties of the page setup objects of all sections to "MultiplePagesType.BOOK-FOLD_PRINTING".
if render_text_as_bookfold:
    for section in doc.sections:
        section = section.as_section()
        section.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
# and the contents will line up in a way that creates a booklet.
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.save_as_pdf_book_fold.pdf', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

