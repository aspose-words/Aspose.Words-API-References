---
title: Document.original_file_name property
linktitle: original_file_name property
articleTitle: original_file_name property
second_title: Aspose.Words for Python
description: "Document.original_file_name property. Gets the original file name of the document."
type: docs
weight: 300
url: /python-net/aspose.words/document/original_file_name/
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
doc = aw.Document(MY_DIR + "Document.docx")

self.assertEqual(MY_DIR + "Document.docx", doc.original_file_name)
self.assertEqual(aw.LoadFormat.DOCX, doc.original_load_format)
```

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
* class [Document](../)

