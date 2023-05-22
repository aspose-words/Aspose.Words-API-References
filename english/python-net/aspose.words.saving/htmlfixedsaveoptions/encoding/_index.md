---
title: HtmlFixedSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML"
type: docs
weight: 30
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---

## HtmlFixedSaveOptions.encoding property

Specifies the encoding to use when exporting to HTML.
Default value is ``new UTF8Encoding(true)`` (UTF-8 with BOM).



### Examples

Shows how to set which encoding to use while exporting a document to HTML.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello World!")

# The default encoding is UTF-8. If we want to represent our document using a different encoding,
# we can use a SaveOptions object to set a specific encoding.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.encoding = "ascii"

self.assertEqual("us-ascii", html_fixed_save_options.encoding)

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.use_encoding.html", html_fixed_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

