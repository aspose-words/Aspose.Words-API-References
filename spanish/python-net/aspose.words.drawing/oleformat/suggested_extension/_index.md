---
title: OleFormat.suggested_extension property
linktitle: suggested_extension property
articleTitle: suggested_extension property
second_title: Aspose.Words for Python
description: "OleFormat.suggested_extension property. Gets the file extension suggested for the current embedded object if you want to save it into a file."
type: docs
weight: 120
url: /es/python-net/aspose.words.drawing/oleformat/suggested_extension/
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
# El objeto OLE en la primera forma es una hoja de cálculo de Microsoft Excel.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# Nuestro objeto no se actualiza automáticamente ni está bloqueado contra actualizaciones.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# Si planeamos guardar el objeto OLE en un archivo en el sistema de archivos local,
# podemos usar la propiedad "SuggestedExtension" para determinar qué extensión de archivo aplicar al archivo.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# A continuación se presentan dos formas de guardar un objeto OLE en un archivo en el sistema de archivos local.
# 1 -  Guardarlo mediante un flujo:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  Guardarlo directamente con un nombre de archivo:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

