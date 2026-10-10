---
title: Document.original_file_name property
linktitle: original_file_name property
articleTitle: original_file_name property
second_title: Aspose.Words for Python
description: "Document.original_file_name property. Gets the original file name of the document."
type: docs
weight: 300
url: /ru/python-net/aspose.words/document/original_file_name/
---

## Document.original_file_name property

Gets the original file name of the document.


```python
@property
def original_file_name(self) -> str:
    ...

```

### Remarks

Returns ``None`` if the document was loaded from a stream or created blank.




### Examples

Shows how to retrieve details of a document's load operation.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
self.assertEqual(MY_DIR + 'Document.docx', doc.original_file_name)
self.assertEqual(aw.LoadFormat.DOCX, doc.original_load_format)
```

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
* class [Document](../)

