﻿---
title: OleFormat.get_raw_data method
linktitle: get_raw_data method
articleTitle: get_raw_data method
second_title: Aspose.Words for Python
description: "OleFormat.get_raw_data method. Gets OLE object raw data."
type: docs
weight: 150
url: /python-net/aspose.words.drawing/oleformat/get_raw_data/
---

## get_raw_data() {#default}

Gets OLE object raw data.


```python
def get_raw_data(self):
    ...
```

### Examples

Shows how to access the raw data of an embedded OLE object.

```python
doc = aw.Document(MY_DIR + 'OLE objects.docx')
for shape in doc.get_child_nodes(aw.NodeType.SHAPE, True):
    ole_format = shape.as_shape().ole_format
    if ole_format is not None:
        if ole_format.is_link:
            print('This is a linked object')
        else:
            print('This is an embedded object')
        ole_raw_data = ole_format.get_raw_data()
        self.assertEqual(24576, len(ole_raw_data))
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

