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
load_options = aw.loading.LoadOptions()
load_options.encoding = system_helper.text.Encoding.ascii()
# Load the document while passing the LoadOptions object, then verify the document's contents.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertTrue('This is a sample text in English.' in doc.to_string(save_format=aw.SaveFormat.TEXT))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

