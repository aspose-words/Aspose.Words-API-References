---
title: OfficeMath.display_type property
linktitle: display_type property
articleTitle: display_type property
second_title: Aspose.Words for Python
description: "OfficeMath.display_type property. Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line."
type: docs
weight: 10
url: /it/python-net/aspose.words.math/officemath/display_type/
---

## OfficeMath.display_type property

Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text
or displayed on its own line.


```python
@property
def display_type(self) -> aspose.words.math.OfficeMathDisplayType:
    ...

@display_type.setter
def display_type(self, value: aspose.words.math.OfficeMathDisplayType):
    ...

```

### Remarks

Display format type has effect for top level Office Math only.

Returned display format type is always [OfficeMathDisplayType.INLINE](../../officemathdisplaytype/#INLINE) for nested Office Math.




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

