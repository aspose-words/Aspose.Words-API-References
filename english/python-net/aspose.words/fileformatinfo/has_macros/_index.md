---
title: FileFormatInfo.has_macros property
linktitle: has_macros property
articleTitle: has_macros property
second_title: Aspose.Words for Python
description: "FileFormatInfo.has_macros property. Returns ``True`` if this document contains a VBA macros."
type: docs
weight: 30
url: /python-net/aspose.words/fileformatinfo/has_macros/
---

## FileFormatInfo.has_macros property

Returns ``True`` if this document contains a VBA macros.



```python
@property
def has_macros(self) -> bool:
    ...

```

### Examples

Shows how to check VBA macro presence without loading document.

```python
file_format_info = aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Macro.docm')
self.assertTrue(file_format_info.has_macros)
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)

