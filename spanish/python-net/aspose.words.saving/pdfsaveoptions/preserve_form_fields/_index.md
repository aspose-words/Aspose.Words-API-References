---
title: PdfSaveOptions.preserve_form_fields property
linktitle: preserve_form_fields property
articleTitle: preserve_form_fields property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.preserve_form_fields property. Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text"
type: docs
weight: 300
url: /es/python-net/aspose.words.saving/pdfsaveoptions/preserve_form_fields/
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
# Inserte un cuadro combinado que permita al usuario elegir una opción de una colección de cadenas.
builder.insert_combo_box('MyComboBox', ['Apple', 'Banana', 'Cherry'], 0)
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
pdf_options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "PreserveFormFields" en "true" para guardar los campos de formulario como objetos interactivos en el PDF de salida.
# Establezca la propiedad "PreserveFormFields" en "false" para congelar todos los campos de formulario en el documento en
# sus valores actuales y mostrarlos como texto plano en el PDF de salida.
pdf_options.preserve_form_fields = preserve_form_fields
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PreserveFormFields.pdf', save_options=pdf_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

