---
title: FileFormatInfo.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "FileFormatInfo.encoding property. Gets the detected encoding if applicable to the current document format"
type: docs
weight: 10
url: /fr/python-net/aspose.words/fileformatinfo/encoding/
---

## FileFormatInfo.encoding property

Gets the detected encoding if applicable to the current document format.
At the moment detects encoding only for HTML documents.


```python
@property
def encoding(self) -> str:
    ...

```

### Examples

Shows how to detect encoding in an html file.

```python
info = aw.FileFormatUtil.detect_file_format(MY_DIR + 'Document.html')
self.assertEqual(aw.LoadFormat.HTML, info.load_format)
# La propriété "encoding" n'est utilisée que lorsque nous créons un objet FileFormatInfo pour un document html.
self.assertEqual('windows-1252', info.encoding)
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)

