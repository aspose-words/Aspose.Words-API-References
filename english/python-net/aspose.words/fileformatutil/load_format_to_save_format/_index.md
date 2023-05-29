---
title: FileFormatUtil.load_format_to_save_format method
linktitle: load_format_to_save_format method
articleTitle: load_format_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.load_format_to_save_format method. Converts a [LoadFormat](../../loadformat/) value to a [SaveFormat](../../saveformat/) value if possible."
type: docs
weight: 70
url: /python-net/aspose.words/fileformatutil/load_format_to_save_format/
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
| System.ArgumentException | Throws when cannot convert. |

### Examples

Shows how to use the aw.FileFormatUtil methods to detect the format of a document.

```python
# Load a document from a file that is missing a file extension, and then detect its file format.
with open(MY_DIR + "Word document with missing file extension", "rb") as doc_stream:

    info = aw.FileFormatUtil.detect_file_format(doc_stream)
    load_format = info.load_format

    self.assertEqual(aw.LoadFormat.DOC, load_format)

    # Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    # 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)

    # 2 -  Convert the LoadFormat directly to its SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)

    # Load a document from the stream, and then save it to the automatically detected file extension.
    doc = aw.Document(doc_stream)

    self.assertEqual(".doc", aw.FileFormatUtil.save_format_to_extension(save_format))

    doc.save(ARTIFACTS_DIR + "File.save_to_detected_file_format" + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

