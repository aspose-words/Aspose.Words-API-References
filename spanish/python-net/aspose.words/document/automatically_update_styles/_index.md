---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /es/python-net/aspose.words/document/automatically_update_styles/
---

## Document.automatically_update_styles property

Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the
attached template each time the document is opened in MS Word.


```python
@property
def automatically_update_styles(self) -> bool:
    ...

@automatically_update_styles.setter
def automatically_update_styles(self, value: bool):
    ...

```

### Examples

Shows how to attach a template to a document.

```python
doc = aw.Document()
# Los documentos de Microsoft Word, por defecto, vienen con una plantilla adjunta llamada "Normal.dotm".
# No hay una plantilla predeterminada para documentos en blanco de Aspose.Words.
self.assertEqual('', doc.attached_template)
# Adjunte una plantilla, luego establezca la bandera para aplicar cambios de estilo
# dentro de la plantilla a los estilos en nuestro documento.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Habilite la actualización automática de estilos, pero no adjunte un documento de plantilla.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Dado que no hay un documento de plantilla, el documento no tenía dónde rastrear los cambios de estilo.
# Utilice un objeto SaveOptions para establecer automáticamente una plantilla
# si un documento que estamos guardando no tiene una.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

