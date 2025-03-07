---
title: PdfSaveOptions.create_note_hyperlinks property
linktitle: create_note_hyperlinks property
articleTitle: create_note_hyperlinks property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.create_note_hyperlinks property. Specifies whether to convert footnote/endnote references in main text story into active hyperlinks"
type: docs
weight: 60
url: /python-net/aspose.words.saving/pdfsaveoptions/create_note_hyperlinks/
---

## PdfSaveOptions.create_note_hyperlinks property

Specifies whether to convert footnote/endnote references in main text story into active hyperlinks.
When clicked the hyperlink will lead to the corresponding footnote/endnote.
Default is ``False``.



```python
@property
def create_note_hyperlinks(self) -> bool:
    ...

@create_note_hyperlinks.setter
def create_note_hyperlinks(self, value: bool):
    ...

```

### Examples

Shows how to make footnotes and endnotes function as hyperlinks.

```python
doc = aw.Document(MY_DIR + 'Footnotes and endnotes.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "create_note_hyperlinks" property to "True" to turn all footnote/endnote symbols
# in the text act as links that, upon clicking, take us to their respective footnotes/endnotes.
# Set the "create_note_hyperlinks" property to "False" not to have footnote/endnote symbols link to anything.
options.create_note_hyperlinks = create_note_hyperlinks
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.note_hyperlinks.pdf', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

