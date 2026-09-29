---
title: CleanupOptions.unused_lists property
linktitle: unused_lists property
articleTitle: unused_lists property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_lists property. Specifies whether unused list and list definitions should be removed from document"
type: docs
weight: 40
url: /es/python-net/aspose.words/cleanupoptions/unused_lists/
---

## CleanupOptions.unused_lists property

Specifies whether unused list and list definitions should be removed from document.
Default value is ``True``.



```python
@property
def unused_lists(self) -> bool:
    ...

@unused_lists.setter
def unused_lists(self, value: bool):
    ...

```

### Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# Combinado con los estilos incorporados, el documento ahora tiene ocho estilos.
# Un estilo personalizado se marca como "used" mientras haya cualquier texto dentro del documento
# formateado con ese estilo. Esto significa que los 4 estilos que añadimos están actualmente sin usar.
self.assertEqual(8, doc.styles.count)
# Aplique un estilo de carácter personalizado y luego un estilo de lista personalizado. Hacerlo los marcará como "used".
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Ahora, hay un estilo de carácter sin usar y un estilo de lista sin usar.
# El método Cleanup() , cuando se configura con un objeto CleanupOptions, puede apuntar a estilos sin usar y eliminarlos.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Eliminar cada nodo al que se aplica un estilo personalizado lo marca como "unused" nuevamente.
# Vuelva a ejecutar el método Cleanup para eliminarlos.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

