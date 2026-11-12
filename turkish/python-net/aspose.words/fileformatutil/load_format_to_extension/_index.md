---
title: FileFormatUtil.load_format_to_extension method
linktitle: load_format_to_extension method
articleTitle: load_format_to_extension method
second_title: Aspose.Words for Python
description: "FileFormatUtil.load_format_to_extension method. Converts a load format enumerated value into a file extension"
type: docs
weight: 60
url: /tr/python-net/aspose.words/fileformatutil/load_format_to_extension/
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
# Dosya uzantısı olmayan bir dosyadan belge yükleyin ve ardından dosya formatını tespit edin.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Aşağıda bir LoadFormat'ı karşılık gelen SaveFormat'a dönüştürmenin iki yöntemi verilmiştir.
    # 1 -  LoadFormat için dosya uzantısı dizesini alın, ardından bu dizeden ilgili SaveFormat'ı alın:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  LoadFormat'ı doğrudan SaveFormat'ına dönüştürün:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Bir belgeyi akıştan yükleyin ve ardından otomatik olarak algılanan dosya uzantısına kaydedin.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

