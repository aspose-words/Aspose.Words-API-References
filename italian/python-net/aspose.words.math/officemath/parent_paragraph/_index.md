---
title: OfficeMath.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "OfficeMath.parent_paragraph property. Retrieves the parent [Paragraph](../../../aspose.words/paragraph/) of this node."
type: docs
weight: 50
url: /it/python-net/aspose.words.math/officemath/parent_paragraph/
---

## OfficeMath.parent_paragraph property

Retrieves the parent [Paragraph](../../../aspose.words/paragraph/) of this node.



```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to set office math display formatting.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# I nodi OfficeMath che sono figli di altri nodi OfficeMath sono sempre in linea.
# Il nodo con cui stiamo lavorando è il nodo base per cambiare la sua posizione e il tipo di visualizzazione.
self.assertEqual(aw.math.MathObjectType.O_MATH_PARA, office_math.math_object_type)
self.assertEqual(aw.NodeType.OFFICE_MATH, office_math.node_type)
self.assertEqual(office_math.parent_node, office_math.parent_paragraph)
# Cambia la posizione e il tipo di visualizzazione del nodo OfficeMath.
office_math.display_type = aw.math.OfficeMathDisplayType.DISPLAY
office_math.justification = aw.math.OfficeMathJustification.LEFT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.OfficeMath.docx')
```

### See Also

* module [aspose.words.math](../../)
* class [OfficeMath](../)

