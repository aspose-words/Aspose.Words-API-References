---
title: LoadOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "LoadOptions.encoding property. Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document"
type: docs
weight: 50
url: /python-net/aspose.words.loading/loadoptions/encoding/
---

## LoadOptions.encoding property

Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified
inside the document.
Can be ``None``. Default is ``None``.



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Remarks

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is ``None``, then the system will try to
automatically detect the encoding.




### Examples

Shows how to set the encoding with which to open a document.

```python
# A FileFormatInfo object will detect this file as being encoded in something other than UTF-7.
file_format_info = aw.FileFormatUtil.detect_file_format(MY_DIR + "Encoded in UTF-7.txt")

self.assertNotEqual("utf-7", file_format_info.encoding)

# If we load the document with no loading configurations, Aspose.Words will detect its encoding as UTF-8.
doc = aw.Document(MY_DIR + "Encoded in UTF-7.txt")

# The contents, parsed in UTF-8, create a valid string.
# However, knowing that the file is in UTF-7, we can see that the result is incorrect.
self.assertEqual("Hello world+ACE-", doc.to_string(aw.SaveFormat.TEXT).strip())

# In cases of ambiguous encoding such as this one, we can set a specific encoding variant
# to parse the file within a LoadOptions object.
load_options = aw.loading.LoadOptions()
load_options.encoding = "utf-7"

# Load the document while passing the LoadOptions object, then verify the document's contents.
doc = aw.Document(MY_DIR + "Encoded in UTF-7.txt", load_options)

self.assertEqual("Hello world!", doc.to_string(aw.SaveFormat.TEXT).strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

