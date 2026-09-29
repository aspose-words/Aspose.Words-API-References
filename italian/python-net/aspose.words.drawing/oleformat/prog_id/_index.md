---
title: OleFormat.prog_id property
linktitle: prog_id property
articleTitle: prog_id property
second_title: Aspose.Words for Python
description: "OleFormat.prog_id property. Gets or sets the ProgID of the OLE object."
type: docs
weight: 90
url: /it/python-net/aspose.words.drawing/oleformat/prog_id/
---

## OleFormat.prog_id property

Gets or sets the ProgID of the OLE object.


```python
@property
def prog_id(self) -> str:
    ...

@prog_id.setter
def prog_id(self, value: str):
    ...

```

### Remarks

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be ``None``.

The default value is an empty string.




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

