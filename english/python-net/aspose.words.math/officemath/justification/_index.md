---
title: OfficeMath.justification property
linktitle: justification property
articleTitle: justification property
second_title: Aspose.Words for Python
description: "OfficeMath.justification property. Gets/sets Office Math justification."
type: docs
weight: 20
url: /python-net/aspose.words.math/officemath/justification/
---

## OfficeMath.justification property

Gets/sets Office Math justification.


```python
@property
def justification(self) -> aspose.words.math.OfficeMathJustification:
    ...

@justification.setter
def justification(self, value: aspose.words.math.OfficeMathJustification):
    ...

```

### Remarks

Justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.INLINE](../../officemathdisplaytype/#INLINE).

Inline justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.DISPLAY](../../officemathdisplaytype/#DISPLAY).

Corresponding [OfficeMath.display_type](../display_type/) has to be set before setting Office Math justification.




### Examples

Shows how to set office math display formatting.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# OfficeMath nodes that are children of other OfficeMath nodes are always inline.
# The node we are working with is the base node to change its location and display type.
self.assertEqual(aw.math.MathObjectType.O_MATH_PARA, office_math.math_object_type)
self.assertEqual(aw.NodeType.OFFICE_MATH, office_math.node_type)
self.assertEqual(office_math.parent_node, office_math.parent_paragraph)
# Change the location and display type of the OfficeMath node.
office_math.display_type = aw.math.OfficeMathDisplayType.DISPLAY
office_math.justification = aw.math.OfficeMathJustification.LEFT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.OfficeMath.docx')
```

### See Also

* module [aspose.words.math](../../)
* class [OfficeMath](../)

