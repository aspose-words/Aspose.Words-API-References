---
title: NodeCollection.insert method
linktitle: insert method
articleTitle: insert method
second_title: Aspose.Words for Python
description: "NodeCollection.insert method. Inserts a node into the collection at the specified index."
type: docs
weight: 70
url: /es/python-net/aspose.words/nodecollection/insert/
---

## insert(index, node) {#int_node}

Inserts a node into the collection at the specified index.


```python
def insert(self, index: int, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | [Node](../../node/) | The node to insert. |

### Remarks

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than [NodeCollection.count](../count/), the node is added at the end of the collection.

If the index is negative and its absolute value is greater than [NodeCollection.count](../count/), the node is added at the end of the collection.




If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(NotSupportedException)) | The [NodeCollection](../) is a "deep" collection. |

### Examples

Shows how to work with a NodeCollection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agrega texto al documento insertando Runs usando un DocumentBuilder.
builder.write('Run 1. ')
builder.write('Run 2. ')
# Cada invocación del método "Write" crea un nuevo Run,
# que luego aparece en la RunCollection del Paragraph padre.
runs = doc.first_section.body.first_paragraph.runs
self.assertEqual(2, runs.count)
# También podemos insertar un nodo en la RunCollection manualmente.
new_run = aw.Run(doc=doc, text='Run 3. ')
runs.insert(3, new_run)
self.assertTrue(runs.contains(new_run))
self.assertEqual('Run 1. Run 2. Run 3.', doc.get_text().strip())
# Accede a los runs individuales y elimínalos para quitar su texto del documento.
run = runs[1]
runs.remove(run)
self.assertEqual('Run 1. Run 3.', doc.get_text().strip())
self.assertIsNotNone(run)
self.assertFalse(runs.contains(run))
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

