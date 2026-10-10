---
title: OleFormat.is_locked property
linktitle: is_locked property
articleTitle: is_locked property
second_title: Aspose.Words for Python
description: "OleFormat.is_locked property. Specifies whether the link to the OLE object is locked from updates."
type: docs
weight: 50
url: /ru/python-net/aspose.words.drawing/oleformat/is_locked/
---

## OleFormat.is_locked property

Specifies whether the link to the OLE object is locked from updates.


```python
@property
def is_locked(self) -> bool:
    ...

@is_locked.setter
def is_locked(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(file_name=MY_DIR + 'OLE spreadsheet.docm')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# OLE-объект в первой фигуре представляет собой электронную таблицу Microsoft Excel.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# Наш объект не обновляется автоматически и не заблокирован от обновлений.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# Если мы планируем сохранять объект OLE в файл в локальной файловой системе,
# мы можем использовать свойство "SuggestedExtension", чтобы определить, какое расширение файла применить к файлу.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# Ниже представлены два способа сохранения объекта OLE в файл в локальной файловой системе.
# 1 -  Сохранить через поток:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  Сохранить напрямую в файл с именем:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

