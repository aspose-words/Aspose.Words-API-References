---
title: NodeList.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "NodeList.count property. Gets the number of nodes in the list."
type: docs
weight: 20
url: /de/python-net/aspose.words/nodelist/count/
---

## NodeList.count property

Gets the number of nodes in the list.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to use XPaths to navigate a NodeList.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie einige Knoten mit einem DocumentBuilder ein.
builder.writeln('Hello world!')
builder.start_table()
builder.insert_cell()
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.end_table()
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Unser Dokument enthält drei Run-Knoten.
node_list = doc.select_nodes('//Run')
self.assertEqual(3, node_list.count)
self.assertTrue(any([n.get_text().strip() == 'Hello world!' for n in node_list]))
self.assertTrue(any([n.get_text().strip() == 'Cell 1' for n in node_list]))
self.assertTrue(any([n.get_text().strip() == 'Cell 2' for n in node_list]))
# Verwenden Sie einen doppelten Vorwärtsschrägstrich, um alle Run-Knoten auszuwählen
# die indirekte Nachkommen eines Table-Knotens sind, also die Runs in den beiden Zellen, die wir eingefügt haben.
node_list = doc.select_nodes('//Table//Run')
self.assertEqual(2, node_list.count)
self.assertTrue(any([n.get_text().strip() == 'Cell 1' for n in node_list]))
self.assertTrue(any([n.get_text().strip() == 'Cell 2' for n in node_list]))
# Einzelne Vorwärtsschrägstriche geben direkte Nachkommenbeziehungen an,
# die wir übersprungen haben, als wir doppelte Schrägstriche verwendeten.
self.assertEqual(doc.select_nodes('//Table//Run'), doc.select_nodes('//Table/Row/Cell/Paragraph/Run'))
# Greifen Sie auf die Form zu, die das Bild enthält, das wir eingefügt haben.
node_list = doc.select_nodes('//Shape')
self.assertEqual(1, node_list.count)
shape = node_list[0].as_shape()
self.assertTrue(shape.has_image)
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

