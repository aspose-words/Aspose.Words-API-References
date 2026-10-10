---
title: OleFormat.suggested_file_name property
linktitle: suggested_file_name property
articleTitle: suggested_file_name property
second_title: Aspose.Words for Python
description: "OleFormat.suggested_file_name property. Gets the file name suggested for the current embedded object if you want to save it into a file."
type: docs
weight: 130
url: /de/python-net/aspose.words.drawing/oleformat/suggested_file_name/
---

## OleFormat.suggested_file_name property

Gets the file name suggested for the current embedded object if you want to save it into a file.


```python
@property
def suggested_file_name(self) -> str:
    ...

```

### Examples

Shows how to get an OLE object's suggested file name.

```python
doc = aw.Document(file_name=MY_DIR + 'OLE shape.rtf')
ole_shape = doc.first_section.body.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# OLE-Objekte können einen vorgeschlagenen Dateinamen und eine Erweiterung bereitstellen,
# die wir beim Speichern des Objektinhalts in einer Datei im lokalen Dateisystem verwenden können.
suggested_file_name = ole_shape.ole_format.suggested_file_name
self.assertEqual('CSV.csv', suggested_file_name)
with system_helper.io.FileStream(ARTIFACTS_DIR + suggested_file_name, system_helper.io.FileMode.CREATE) as file_stream:
    ole_shape.ole_format.save(stream=file_stream)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

