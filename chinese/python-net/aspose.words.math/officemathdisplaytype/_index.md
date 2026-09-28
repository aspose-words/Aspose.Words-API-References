---
title: OfficeMathDisplayType enumeration
linktitle: OfficeMathDisplayType enumeration
articleTitle: OfficeMathDisplayType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.math.OfficeMathDisplayType enumeration. Specifies the display format type of the equation."
type: docs
weight: 30
url: /zh/python-net/aspose.words.math/officemathdisplaytype/
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
# 作为其他 OfficeMath 节点子节点的 OfficeMath 节点始终是内联的。
# 我们正在处理的节点是用于更改其位置和显示类型的基础节点。
self.assertEqual(aw.math.MathObjectType.O_MATH_PARA, office_math.math_object_type)
self.assertEqual(aw.NodeType.OFFICE_MATH, office_math.node_type)
self.assertEqual(office_math.parent_node, office_math.parent_paragraph)
# 更改 OfficeMath 节点的位置和显示类型。
office_math.display_type = aw.math.OfficeMathDisplayType.DISPLAY
office_math.justification = aw.math.OfficeMathJustification.LEFT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.OfficeMath.docx')
```

### See Also

* module [aspose.words.math](../)

