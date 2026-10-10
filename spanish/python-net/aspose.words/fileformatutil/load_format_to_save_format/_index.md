---
title: FileFormatUtil.load_format_to_save_format method
linktitle: load_format_to_save_format method
articleTitle: load_format_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.load_format_to_save_format method. Converts a [LoadFormat](../../loadformat/) value to a [SaveFormat](../../saveformat/) value if possible."
type: docs
weight: 70
url: /es/python-net/aspose.words/fileformatutil/load_format_to_save_format/
---

## load_format_to_save_format(load_format) {#loadformat}

Converts a [LoadFormat](../../loadformat/) value to a [SaveFormat](../../saveformat/) value if possible.



```python
def load_format_to_save_format(self, load_format: aspose.words.LoadFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| load_format | [LoadFormat](../../loadformat/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# Cargue un documento desde un archivo que carece de extensión y luego detecte su formato de archivo.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # A continuación se presentan dos métodos para convertir un LoadFormat a su correspondiente SaveFormat.
    # 1 -  Obtenga la cadena de extensión de archivo para el LoadFormat, luego obtenga el SaveFormat correspondiente a partir de esa cadena:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Convierta el LoadFormat directamente a su SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Cargue un documento desde el flujo y luego guárdelo con la extensión de archivo detectada automáticamente.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

