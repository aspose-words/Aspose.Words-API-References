---
title: OleFormat.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.OleFormat.save method"
type: docs
weight: 160
url: /python-net/aspose.words.drawing/oleformat/save/
---

## save(stream) {#bytesio}

Saves the data of the embedded object into the specified stream.


```python
def save(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

It is the responsibility of the caller to dispose the stream.




### Exceptions

| exception | condition |
| --- | --- |
| System.InvalidOperationException | Throws if you attempt to save a linked object. |

## save(file_name) {#str}

Saves the data of the embedded object into a file with the specified name.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

### Exceptions

| exception | condition |
| --- | --- |
| System.InvalidOperationException | Throws if you attempt to save a linked object. |

## Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(MY_DIR + "OLE spreadsheet.docm")
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

# The OLE object in the first shape is a Microsoft Excel spreadsheet.
ole_format = shape.ole_format

self.assertEqual("Excel.Sheet.12", ole_format.prog_id)

# Our object is neither auto updating nor locked from updates.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)

# If we plan on saving the OLE object to a file in the local file system,
# we can use the "suggested_extension" property to determine which file extension to apply to the file.
self.assertEqual(".xlsx", ole_format.suggested_extension)

# Below are two ways of saving an OLE object to a file in the local file system.
# 1 -  Save it via a stream:
with open(ARTIFACTS_DIR + "OLE spreadsheet extracted via stream" + ole_format.suggested_extension, "wb") as file:
    ole_format.save(file)

# 2 -  Save it directly to a filename:
ole_format.save(ARTIFACTS_DIR + "OLE spreadsheet saved directly" + ole_format.suggested_extension)
```

## See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

