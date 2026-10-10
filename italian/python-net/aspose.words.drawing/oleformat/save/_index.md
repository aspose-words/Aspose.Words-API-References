---
title: OleFormat.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.OleFormat.save method"
type: docs
weight: 160
url: /it/python-net/aspose.words.drawing/oleformat/save/
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
# L'oggetto OLE nella prima forma è un foglio di calcolo Microsoft Excel.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# Il nostro oggetto non si aggiorna automaticamente né è bloccato dagli aggiornamenti.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# Se prevediamo di salvare l'oggetto OLE in un file nel file system locale,
# possiamo usare la proprietà "SuggestedExtension" per determinare quale estensione di file applicare al file.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# Di seguito sono riportati due modi per salvare un oggetto OLE in un file nel file system locale.
# 1 -  Salvalo tramite uno stream:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  Salvalo direttamente in un nome file:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

## See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

