---
title: XpsSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 20
url: /python-net/aspose.words.saving/xpssaveoptions/compression_level/
---

## XpsSaveOptions.compression_level property

Specifies the compression level used to save document.
The default value is [CompressionLevel.NORMAL](../../compressionlevel/#NORMAL).



```python
@property
def compression_level(self) -> aspose.words.saving.CompressionLevel:
    ...

@compression_level.setter
def compression_level(self, value: aspose.words.saving.CompressionLevel):
    ...

```

### Examples

Shows how to control the compression level when saving a document to XPS format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Sample document for XPS compression test.')
# Create an XpsSaveOptions object and set the compression level.
options = aw.saving.XpsSaveOptions()
options.compression_level = aw.saving.CompressionLevel.MAXIMUM
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.CompressionLevelXps.xps', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

