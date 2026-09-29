---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /es/python-net/aspose.words.loading/txtloadoptions/document_direction/
---

## TxtLoadOptions.document_direction property

Gets or sets a document direction.
The default value is [DocumentDirection.LEFT_TO_RIGHT](../../documentdirection/#LEFT_TO_RIGHT).



```python
@property
def document_direction(self) -> aspose.words.loading.DocumentDirection:
    ...

@document_direction.setter
def document_direction(self, value: aspose.words.loading.DocumentDirection):
    ...

```

### Examples

Shows how to detect plaintext document text direction.

```python
# Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
# para modificar cómo cargamos un documento de texto sin formato.
load_options = aw.loading.TxtLoadOptions()
# Establezca la propiedad "DocumentDirection" a "DocumentDirection.Auto" para que detecte automáticamente
# la dirección de cada párrafo de texto que Aspose.Words carga desde texto sin formato.
# La propiedad "Bidi" de cada párrafo almacenará su dirección.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Detecte texto hebreo como de derecha a izquierda.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Detecte texto inglés como de derecha a izquierda.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

