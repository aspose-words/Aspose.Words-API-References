---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /python-net/aspose.words.saving/pssaveoptions/save_format/
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
doc = aw.Document(MY_DIR + 'Paragraphs.docx')
# Create a "PsSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to PostScript.
# Set the "use_book_fold_printing_settings" property to "True" to arrange the contents
# in the output Postscript document in a way that helps us make a booklet out of it.
# Set the "use_book_fold_printing_settings" property to "False" to save the document normally.
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# If we are rendering the document as a booklet, we must set the "multiple_pages"
# properties of the page setup objects of all sections to "MultiplePagesType.BOOK_FOLD_PRINTING".
for section in doc.sections:
    section = section.as_section()
    section.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
# and the contents will line up in a way that creates a booklet.
doc.save(ARTIFACTS_DIR + 'PsSaveOptions.use_book_fold_printing_settings.ps', save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

