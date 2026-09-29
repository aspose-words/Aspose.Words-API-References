---
title: PdfSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "PdfSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 390
url: /es/python-net/aspose.words.saving/pdfsaveoptions/clone/
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
# Insertar texto con los campos PAGE y NUMPAGES. Estos campos no muestran el valor correcto en tiempo real.
# Necesitaremos actualizarlos manualmente usando métodos de actualización como "Field.Update()" y "Document.UpdateFields()"
# cada vez que necesitemos que muestren valores precisos.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "UpdateFields" en "false" para no actualizar todos los campos de un documento justo antes de una operación de guardado.
# Esta es la opción preferible si sabemos que todos nuestros campos estarán actualizados antes de guardar.
# Establezca la propiedad "UpdateFields" en "true" para iterar a través de todo el documento
# campos y actualizarlos antes de guardarlo como PDF. Esto asegurará que todos los campos muestren
# los valores más precisos en el PDF.
options.update_fields = update_fields
# Podemos clonar objetos PdfSaveOptions.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

