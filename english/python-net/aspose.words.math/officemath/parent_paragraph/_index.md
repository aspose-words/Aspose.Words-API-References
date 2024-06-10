---
title: OfficeMath.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "OfficeMath.parent_paragraph property. Retrieves the parent [Paragraph](../../../aspose.words/paragraph/) of this node."
type: docs
weight: 50
url: /python-net/aspose.words.math/officemath/parent_paragraph/
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
doc = aw.Document(MY_DIR + 'Office math.docx')
office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# OfficeMath nodes that are children of other OfficeMath nodes are always inline.
# The node we are working with is the base node to change its location and display type.
self.assertEqual(aw.math.MathObjectType.O_MATH_PARA, office_math.math_object_type)
self.assertEqual(aw.NodeType.OFFICE_MATH, office_math.node_type)
self.assertEqual(office_math.parent_node, office_math.parent_paragraph)
# Change the location and display type of the OfficeMath node.
office_math.display_type = aw.math.OfficeMathDisplayType.DISPLAY
office_math.justification = aw.math.OfficeMathJustification.LEFT
doc.save(ARTIFACTS_DIR + 'Shape.office_math.docx')
```

### See Also

* module [aspose.words.math](../../)
* class [OfficeMath](../)

