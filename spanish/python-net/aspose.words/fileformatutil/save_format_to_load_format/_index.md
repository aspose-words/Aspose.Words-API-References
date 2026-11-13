---
title: FileFormatUtil.save_format_to_load_format method
linktitle: save_format_to_load_format method
articleTitle: save_format_to_load_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.save_format_to_load_format method. Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible."
type: docs
weight: 90
url: /es/python-net/aspose.words/fileformatutil/save_format_to_load_format/
---

## save_format_to_load_format(save_format) {#saveformat}

Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible.



```python
def save_format_to_load_format(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../saveformat/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to convert a save format to its corresponding load format.

```python
self.assertEqual(aw.LoadFormat.HTML, aw.FileFormatUtil.save_format_to_load_format(aw.SaveFormat.HTML))
# Algunos tipos de archivo pueden tener documentos guardados, pero no cargados usando Aspose.Words.
# Si intentamos convertir un formato de guardado de ese tipo a un formato de carga, se lanzará una excepción.
self.assertRaises(Exception, lambda: aw.FileFormatUtil.save_format_to_load_format(aw.SaveFormat.JPEG))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

