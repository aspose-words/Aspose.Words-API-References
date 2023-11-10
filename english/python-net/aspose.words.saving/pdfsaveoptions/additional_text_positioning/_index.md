---
title: PdfSaveOptions.additional_text_positioning property
linktitle: additional_text_positioning property
articleTitle: additional_text_positioning property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.additional_text_positioning property. A flag specifying whether to write additional text positioning operators or not."
type: docs
weight: 20
url: /python-net/aspose.words.saving/pdfsaveoptions/additional_text_positioning/
---

## PdfSaveOptions.additional_text_positioning property

A flag specifying whether to write additional text positioning operators or not.


```python
@property
def additional_text_positioning(self) -> bool:
    ...

@additional_text_positioning.setter
def additional_text_positioning(self, value: bool):
    ...

```

### Remarks

If ``True``, additional text positioning operators are written to the output PDF. This may help to overcome
issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.


The default value is ``False``.




### Examples

Show how to write additional text positioning operators.

```python
doc = aw.Document(MY_DIR + "Text positioning operators.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.text_compression = aw.saving.PdfTextCompression.NONE

# Set the "additional_text_positioning" property to "True" to attempt to fix incorrect
# element positioning in the output PDF, should there be any, at the cost of increased file size.
# Set the "additional_text_positioning" property to "False" to render the document as usual.
save_options.additional_text_positioning = apply_additional_text_positioning

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.additional_text_positioning.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

