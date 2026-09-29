---
title: FileFormatUtil.load_format_to_extension method
linktitle: load_format_to_extension method
articleTitle: load_format_to_extension method
second_title: Aspose.Words for Python
description: "FileFormatUtil.load_format_to_extension method. Converts a load format enumerated value into a file extension"
type: docs
weight: 60
url: /sv/python-net/aspose.words/fileformatutil/load_format_to_extension/
---

## load_format_to_extension(load_format) {#loadformat}

Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.


```python
def load_format_to_extension(self, load_format: aspose.words.LoadFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| load_format | [LoadFormat](../../loadformat/) |  |

### Remarks

The [SaveFormat.WORD_ML](../../saveformat/#WORD_ML) value is converted to ".wml".




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# Läs in ett dokument från en fil som saknar filändelse och upptäck sedan dess filformat.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Nedan följer två metoder för att konvertera ett LoadFormat till dess motsvarande SaveFormat.
    # 1 -  Hämta filändelse‑strängen för LoadFormat, och hämta sedan motsvarande SaveFormat från den strängen:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Konvertera LoadFormat direkt till dess SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Läs in ett dokument från strömmen och spara sedan det till den automatiskt upptäckta filändelsen.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

