---
title: Document.remove_personal_information property
linktitle: remove_personal_information property
articleTitle: remove_personal_information property
second_title: Aspose.Words for Python
description: "Document.remove_personal_information property. Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document."
type: docs
weight: 370
url: /es/python-net/aspose.words/document/remove_personal_information/
---

## Document.remove_personal_information property

Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and
document properties upon saving the document.


```python
@property
def remove_personal_information(self) -> bool:
    ...

@remove_personal_information.setter
def remove_personal_information(self, value: bool):
    ...

```

### Examples

Shows how to enable the removal of personal information during a manual save.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte contenido con información personal.
doc.built_in_document_properties.author = 'John Doe'
doc.built_in_document_properties.company = 'Placeholder Inc.'
doc.start_track_revisions(author=doc.built_in_document_properties.author, date_time=datetime.datetime.now())
builder.write('Hello world!')
doc.stop_track_revisions()
# Esta bandera equivale a Archivo -> Opciones -> Centro de confianza -> Configuración del Centro de confianza... ->
# Opciones de privacidad -> "Eliminar información personal de las propiedades del archivo al guardar" en Microsoft Word.
doc.remove_personal_information = save_without_personal_info
# Esta opción no tendrá efecto durante una operación de guardado realizada con Aspose.Words.
# Los datos personales se eliminarán de nuestro documento con la bandera activada cuando lo guardemos manualmente usando Microsoft Word.
doc.save(file_name=ARTIFACTS_DIR + 'Document.RemovePersonalInformation.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.RemovePersonalInformation.docx')
self.assertEqual(save_without_personal_info, doc.remove_personal_information)
self.assertEqual('John Doe', doc.built_in_document_properties.author)
self.assertEqual('Placeholder Inc.', doc.built_in_document_properties.company)
self.assertEqual('John Doe', doc.revisions[0].author)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

