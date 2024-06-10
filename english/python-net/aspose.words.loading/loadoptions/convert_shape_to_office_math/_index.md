---
title: LoadOptions.convert_shape_to_office_math property
linktitle: convert_shape_to_office_math property
articleTitle: convert_shape_to_office_math property
second_title: Aspose.Words for Python
description: "LoadOptions.convert_shape_to_office_math property. Gets or sets whether to convert shapes with EquationXML to Office Math objects."
type: docs
weight: 40
url: /python-net/aspose.words.loading/loadoptions/convert_shape_to_office_math/
---

## LoadOptions.convert_shape_to_office_math property

Gets or sets whether to convert shapes with EquationXML to Office Math objects.


```python
@property
def convert_shape_to_office_math(self) -> bool:
    ...

@convert_shape_to_office_math.setter
def convert_shape_to_office_math(self, value: bool):
    ...

```

### Examples

Shows how to convert EquationXML shapes to Office Math objects.

```python
load_options = aw.loading.LoadOptions()
# Use this flag to specify whether to convert the shapes with EquationXML attributes
# to Office Math objects and then load the document.
load_options.convert_shape_to_office_math = is_convert_shape_to_office_math
doc = aw.Document(MY_DIR + 'Math shapes.docx', load_options)
if is_convert_shape_to_office_math:
    self.assertEqual(16, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
    self.assertEqual(34, doc.get_child_nodes(aw.NodeType.OFFICE_MATH, True).count)
else:
    self.assertEqual(24, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
    self.assertEqual(0, doc.get_child_nodes(aw.NodeType.OFFICE_MATH, True).count)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

