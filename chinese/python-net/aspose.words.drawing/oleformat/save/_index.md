---
title: OleFormat.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.OleFormat.save method"
type: docs
weight: 160
url: /zh/python-net/aspose.words.drawing/oleformat/save/
---

## save(stream) {#bytesio}

Saves the data of the embedded object into the specified stream.


```python
def save(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Where to save the object data. |

### Remarks

It is the responsibility of the caller to dispose the stream.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if you attempt to save a linked object. |

## save(file_name) {#str}

Saves the data of the embedded object into a file with the specified name.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Name of the file to save the OLE object data. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if you attempt to save a linked object. |

## Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(file_name=MY_DIR + 'OLE spreadsheet.docm')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# 第一个形状中的 OLE 对象是 Microsoft Excel 电子表格。
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# 我们的对象既不自动更新，也未锁定更新。
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# 如果我们计划将 OLE 对象保存到本地文件系统中的文件，
# 我们可以使用 "SuggestedExtension" 属性来确定应为文件使用的扩展名。
self.assertEqual('.xlsx', ole_format.suggested_extension)
# 下面提供了两种将 OLE 对象保存到本地文件系统中文件的方法。
# 1 -  通过流保存：
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  直接保存到文件名：
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

## See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

