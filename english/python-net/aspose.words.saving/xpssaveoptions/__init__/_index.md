---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/xpssaveoptions/__init__/
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
doc = aw.Document(MY_DIR + 'Paragraphs.docx')
# Create an "XpsSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .XPS.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# Set the "use_book_fold_printing_settings" property to "True" to arrange the contents
# in the output XPS in a way that helps us use it to make a booklet.
# Set the "use_book_fold_printing_settings" property to "False" to render the XPS normally.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# If we are rendering the document as a booklet, we must set the "multiple_pages"
# properties of the page setup objects of all sections to "MultiplePagesType.BOOK_FOLD_PRINTING".
if render_text_as_book_fold:
    for section in doc.sections:
        section = section.as_section()
        section.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Once we print this document, we can turn it into a booklet by stacking the pages
# to come out of the printer and folding down the middle.
doc.save(ARTIFACTS_DIR + 'XpsSaveOptions.book_fold.xps', xps_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

