---
title: PdfSaveOptions.preserve_form_fields property
linktitle: preserve_form_fields property
articleTitle: preserve_form_fields property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.preserve_form_fields property. Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text"
type: docs
weight: 270
url: /python-net/aspose.words.saving/pdfsaveoptions/preserve_form_fields/
---

## PdfSaveOptions.preserve_form_fields property

Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text.
Default is ``False``.


Microsoft Word form fields include text input, drop down and check box controls.

When set to ``False``, these fields will be exported as text to PDF. When set to ``True``,
these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form
fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are
inline objects.

Editable forms are prohibited by PDF/A compliance. ``False`` value will be used automatically
when saving to PDF/A.

Form fields are not supported when saving to PDF/UA. ``False`` value will be used automatically.




### Examples

Shows how to save a document to the PDF format using the Save method and the PdfSaveOptions class.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Please select a fruit: ")

# Insert a combo box which will allow a user to choose an option from a collection of strings.
builder.insert_combo_box("MyComboBox", ["Apple", "Banana", "Cherry"], 0)

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
pdf_options = aw.saving.PdfSaveOptions()

# Set the "preserve_form_fields" property to "True" to save form fields as interactive objects in the output PDF.
# Set the "preserve_form_fields" property to "False" to freeze all form fields in the document at
# their current values and display them as plain text in the output PDF.
pdf_options.preserve_form_fields = preserve_form_fields

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.preserve_form_fields.pdf", pdf_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

