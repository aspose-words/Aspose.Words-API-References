---
title: OfficeMathDisplayType enumeration
linktitle: OfficeMathDisplayType enumeration
articleTitle: OfficeMathDisplayType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.math.OfficeMathDisplayType enumeration. Specifies the display format type of the equation."
type: docs
weight: 30
url: /python-net/aspose.words.math/officemathdisplaytype/
---

## OfficeMathDisplayType enumeration

Specifies the display format type of the equation.


### Members

| Name | Description |
| --- | --- |
| DISPLAY | The Office Math is displayed on its own line. |
| INLINE | The Office Math is displayed inline with the text. |

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

* module [aspose.words.math](../)

