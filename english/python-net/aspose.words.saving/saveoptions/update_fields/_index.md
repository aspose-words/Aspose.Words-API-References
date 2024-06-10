---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 140
url: /python-net/aspose.words.saving/saveoptions/update_fields/
---

## SaveOptions.update_fields property

Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format.
Default value for this property is ``True``.



```python
@property
def update_fields(self) -> bool:
    ...

@update_fields.setter
def update_fields(self, value: bool):
    ...

```

### Remarks

Allows to specify whether to mimic or not MS Word behavior.


### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
# We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
# each time we need them to display accurate values.
builder.write('Page ')
builder.insert_field('PAGE', '')
builder.write(' of ')
builder.insert_field('NUMPAGES', '')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "update_fields" property to "False" to not update all the fields in a document right before a save operation.
# This is the preferable option if we know that all our fields will be up to date before saving.
# Set the "update_fields" property to "True" to iterate through all the document
# fields and update them before we save it as a PDF. This will make sure that all the fields will display
# the most accurate values in the PDF.
options.update_fields = update_fields
# We can clone PdfSaveOptions objects.
options_copy = options.clone()
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.update_fields.pdf', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

