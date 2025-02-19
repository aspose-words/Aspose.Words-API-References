﻿---
title: OleFormat.suggested_extension property
linktitle: suggested_extension property
articleTitle: suggested_extension property
second_title: Aspose.Words for Python
description: "OleFormat.suggested_extension property. Gets the file extension suggested for the current embedded object if you want to save it into a file."
type: docs
weight: 120
url: /python-net/aspose.words.drawing/oleformat/suggested_extension/
---

## OleFormat.suggested_extension property

Gets the file extension suggested for the current embedded object if you want to save it into a file.


```python
@property
def suggested_extension(self) -> str:
    ...

```

### Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(file_name=MY_DIR + 'OLE spreadsheet.docm')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# The OLE object in the first shape is a Microsoft Excel spreadsheet.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# Our object is neither auto updating nor locked from updates.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# If we plan on saving the OLE object to a file in the local file system,
# we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# Below are two ways of saving an OLE object to a file in the local file system.
# 1 -  Save it via a stream:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  Save it directly to a filename:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

