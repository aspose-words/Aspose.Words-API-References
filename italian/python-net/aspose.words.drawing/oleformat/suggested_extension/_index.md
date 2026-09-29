---
title: OleFormat.suggested_extension property
linktitle: suggested_extension property
articleTitle: suggested_extension property
second_title: Aspose.Words for Python
description: "OleFormat.suggested_extension property. Gets the file extension suggested for the current embedded object if you want to save it into a file."
type: docs
weight: 120
url: /it/python-net/aspose.words.drawing/oleformat/suggested_extension/
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

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

