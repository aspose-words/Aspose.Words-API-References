---
title: FileFormatUtil.extension_to_save_format method
linktitle: extension_to_save_format method
articleTitle: extension_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.extension_to_save_format method. Converts a file name extension into a [SaveFormat](../../saveformat/) value."
type: docs
weight: 40
url: /ru/python-net/aspose.words/fileformatutil/extension_to_save_format/
---

## extension_to_save_format(extension) {#str}

Converts a file name extension into a [SaveFormat](../../saveformat/) value.



```python
def extension_to_save_format(self, extension: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| extension | str | The file extension. Can be with or without a leading dot. Case-insensitive. |

### Remarks

If the extension cannot be recognized, returns [SaveFormat.UNKNOWN](../../saveformat/#UNKNOWN).




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws if the parameter is ``None``. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# Загрузите документ из файла без расширения и затем определите его формат.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Ниже представлены два метода преобразования LoadFormat в соответствующий SaveFormat.
    # 1 -  Получите строку расширения файла для LoadFormat, затем получите соответствующий SaveFormat из этой строки:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Преобразуйте LoadFormat напрямую в его SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Загрузите документ из потока, а затем сохраните его с автоматически определённым расширением файла.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

