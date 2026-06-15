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



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Examples

Shows how to set which encoding to use while exporting a document to HTML.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
from pathlib import Path
import re
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello World!')
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.encoding = 'US-ASCII'
self.assertEqual('US-ASCII', html_fixed_save_options.encoding)
doc.save(file_name=ARTIFACTS_DIR + 'HtmlFixedSaveOptions.UseEncoding.html', save_options=html_fixed_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

