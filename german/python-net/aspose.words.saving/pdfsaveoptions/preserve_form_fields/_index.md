---
title: PdfSaveOptions.preserve_form_fields property
linktitle: preserve_form_fields property
articleTitle: preserve_form_fields property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.preserve_form_fields property. Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text"
type: docs
weight: 300
url: /de/python-net/aspose.words.saving/pdfsaveoptions/preserve_form_fields/
---

## PdfSaveOptions.preserve_form_fields property

Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text.
Default is ``False``.



```python
@property
def preserve_form_fields(self) -> bool:
    ...

@preserve_form_fields.setter
def preserve_form_fields(self, value: bool):
    ...

```

### Remarks

Microsoft Word form fields include text input, drop down and check box controls.

When set to ``False``, these fields will be exported as text to PDF. When set to ``True``,
these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form
fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are
inline objects.




### Examples

Shows how to save a document to the PDF format using the Save method and the PdfSaveOptions class.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please select a fruit: ')
# Fügen Sie ein Kombinationsfeld ein, das einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenketten auszuwählen.
builder.insert_combo_box('MyComboBox', ['Apple', 'Banana', 'Cherry'], 0)
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
pdf_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "PreserveFormFields" auf "true", um Formularfelder als interaktive Objekte im Ausgabe‑PDF zu speichern.
# Setzen Sie die Eigenschaft "PreserveFormFields" auf "false", um alle Formularfelder im Dokument bei
# ihren aktuellen Werten zu fixieren und sie als Klartext im Ausgabe‑PDF anzuzeigen.
pdf_options.preserve_form_fields = preserve_form_fields
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PreserveFormFields.pdf', save_options=pdf_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

