---
title: TxtSaveOptionsBase.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.encoding property. Specifies the encoding to use when exporting in text formats"
type: docs
weight: 10
url: /python-net/aspose.words.saving/txtsaveoptionsbase/encoding/
---

## TxtSaveOptionsBase.encoding property

Specifies the encoding to use when exporting in text formats. 
Default value is **Encoding.UTF8**.



### Examples

Shows how to set encoding for a .txt output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add some text with characters from outside the ASCII character set.
builder.write("À È Ì Ò Ù.")

# Create a "TxtSaveOptions" object, which we can pass to the document's "save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()

# Verify that the "encoding" property contains the appropriate encoding for our document's contents.
self.assertEqual("utf-8", txt_save_options.encoding)

doc.save(ARTIFACTS_DIR + "TxtSaveOptions.encoding.utf8.txt", txt_save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.encoding.utf8.txt", "rb") as file:
    doc_text = file.read().decode('utf-8')

self.assertEqual("\uFEFFÀ È Ì Ò Ù.\r\n", doc_text)

# Using an unsuitable encoding may result in a loss of document contents.
txt_save_options.encoding = "ascii"
doc.save(ARTIFACTS_DIR + "TxtSaveOptions.encoding.ascii.txt", txt_save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.Encoding.ascii.txt", "rb") as file:
    doc_text = file.read().decode('ascii')

self.assertEqual("? ? ? ? ?.\r\n", doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

