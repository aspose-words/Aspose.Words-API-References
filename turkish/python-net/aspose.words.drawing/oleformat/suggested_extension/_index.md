---
title: OleFormat.suggested_extension property
linktitle: suggested_extension property
articleTitle: suggested_extension property
second_title: Aspose.Words for Python
description: "OleFormat.suggested_extension property. Gets the file extension suggested for the current embedded object if you want to save it into a file."
type: docs
weight: 120
url: /tr/python-net/aspose.words.drawing/oleformat/suggested_extension/
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
# İlk şekildeki OLE nesnesi bir Microsoft Excel elektronik tablosudur.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# Nesnemiz ne otomatik güncelleniyor ne de güncellemelerden kilitli.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# Eğer OLE nesnesini yerel dosya sisteminde bir dosyaya kaydetmeyi planlıyorsak,
# dosyaya uygulanacak dosya uzantısını belirlemek için "SuggestedExtension" özelliğini kullanabiliriz.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# Aşağıda OLE nesnesini yerel dosya sisteminde bir dosyaya kaydetmenin iki yolu verilmiştir.
# 1 -  Akış üzerinden kaydedin:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  Doğrudan bir dosya adına kaydedin:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

