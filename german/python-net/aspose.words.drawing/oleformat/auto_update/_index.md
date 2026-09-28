---
title: OleFormat.auto_update property
linktitle: auto_update property
articleTitle: auto_update property
second_title: Aspose.Words for Python
description: "OleFormat.auto_update property. Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word."
type: docs
weight: 10
url: /de/python-net/aspose.words.drawing/oleformat/auto_update/
---

## OleFormat.auto_update property

Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word.


```python
@property
def auto_update(self) -> bool:
    ...

@auto_update.setter
def auto_update(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(file_name=MY_DIR + 'OLE spreadsheet.docm')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# Unser Objekt wird weder automatisch aktualisiert noch vor Updates gesperrt.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# Wenn wir planen, das OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern,
# können wir die Eigenschaft "SuggestedExtension" verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# Im Folgenden sind zwei Methoden zum Speichern eines OLE-Objekts in einer Datei im lokalen Dateisystem aufgeführt.
# 1 -  Speichern Sie es über einen Stream:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  Speichern Sie es direkt unter einem Dateinamen:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

