---
title: OfficeMath.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "OfficeMath.node_type property. Returns [NodeType.OFFICE_MATH](../../../aspose.words/nodetype/#OFFICE_MATH)."
type: docs
weight: 40
url: /zh/python-net/aspose.words.math/officemath/node_type/
---

## OfficeMath.node_type property

Returns [NodeType.OFFICE_MATH](../../../aspose.words/nodetype/#OFFICE_MATH).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

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

* module [aspose.words.math](../../)
* class [OfficeMath](../)

