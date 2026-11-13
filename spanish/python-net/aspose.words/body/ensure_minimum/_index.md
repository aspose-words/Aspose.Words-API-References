---
title: Body.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Body.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 70
url: /es/python-net/aspose.words/body/ensure_minimum/
---

## ensure_minimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Clears main text from all sections from the document leaving the sections themselves.

```python
doc = aw.Document()
# Un documento en blanco contiene una sección, un cuerpo y un párrafo.
# Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
# y terminará con un nodo de documento sin hijos.
doc.remove_all_children()
# Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
# Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
# Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
section = aw.Section(doc)
doc.append_child(section)
# Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
# en la página entre el encabezado y el pie de página de la sección.
body = aw.Body(doc)
section.append_child(body)
# Este cuerpo no tiene hijos, por lo que no podemos añadir runs aún.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# Llame a "EnsureMinimum" para asegurarse de que este cuerpo contenga al menos un párrafo vacío.
body.ensure_minimum()
# Ahora, podemos añadir runs al cuerpo y hacer que el documento los muestre.
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Body](../)

