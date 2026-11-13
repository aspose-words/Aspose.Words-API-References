---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /es/python-net/aspose.words.loading/documentdirection/
---

## DocumentDirection enumeration

Allows to specify the direction to flow the text in a document.


### Members

| Name | Description |
| --- | --- |
| LEFT_TO_RIGHT | Left to right direction. |
| RIGHT_TO_LEFT | Right to left direction. |
| AUTO | Auto-detect direction. |

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

* module [aspose.words.loading](../)

