---
title: PdfSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "PdfSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 380
url: /python-net/aspose.words.saving/pdfsaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```python
def clone(self):
    ...
```

### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
# We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
# each time we need them to display accurate values.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
# This is the preferable option if we know that all our fields will be up to date before saving.
# Set the "UpdateFields" property to "true" to iterate through all the document
# fields and update them before we save it as a PDF. This will make sure that all the fields will display
# the most accurate values in the PDF.
options.update_fields = update_fields
# We can clone PdfSaveOptions objects.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

