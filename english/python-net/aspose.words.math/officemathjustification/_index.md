---
title: OfficeMathJustification enumeration
linktitle: OfficeMathJustification enumeration
articleTitle: OfficeMathJustification enumeration
second_title: Aspose.Words for Python
description: "aspose.words.math.OfficeMathJustification enumeration. Specifies the justification of the equation."
type: docs
weight: 40
url: /python-net/aspose.words.math/officemathjustification/
---

## OfficeMathJustification enumeration

Specifies the justification of the equation.


### Members

| Name | Description |
| --- | --- |
| CENTER_GROUP | Justifies instances of mathematical text to the left with respect to each other, and centers the group of mathematical text (the Math Paragraph) with respect to the page. |
| CENTER | Centers each instance of mathematical text individually with respect to margins. |
| LEFT | Left justification of Math Paragraph. |
| RIGHT | Right Justification of Math Paragraph. |
| INLINE | Inline position of Math. |
| DEFAULT | Default value [OfficeMathJustification.CENTER_GROUP](./#CENTER_GROUP). |

### Examples

Shows how to set office math display formatting.

```python
doc = aw.Document(MY_DIR + "Office math.docx")

office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()

# OfficeMath nodes that are children of other OfficeMath nodes are always inline.
# The node we are working with is the base node to change its location and display type.
self.assertEqual(aw.math.MathObjectType.O_MATH_PARA, office_math.math_object_type)
self.assertEqual(aw.NodeType.OFFICE_MATH, office_math.node_type)
self.assertEqual(office_math.parent_node, office_math.parent_paragraph)

# Change the location and display type of the OfficeMath node.
office_math.display_type = aw.math.OfficeMathDisplayType.DISPLAY
office_math.justification = aw.math.OfficeMathJustification.LEFT

doc.save(ARTIFACTS_DIR + "Shape.office_math.docx")
```

### See Also

* module [aspose.words.math](../)

