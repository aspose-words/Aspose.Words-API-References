---
title: LayoutOptions.enable_text_shaping property
linktitle: enable_text_shaping property
articleTitle: enable_text_shaping property
second_title: Aspose.Words for Python
description: "LayoutOptions.enable_text_shaping property. Flag indicating whether to enable support for OpenType features using the HarfBuzz text shaping engine."
type: docs
weight: 50
url: /python-net/aspose.words.layout/layoutoptions/enable_text_shaping/
---

## LayoutOptions.enable_text_shaping property

Flag indicating whether to enable support for OpenType features using the HarfBuzz text shaping engine.


```python
@property
def enable_text_shaping(self) -> bool:
    ...

@enable_text_shaping.setter
def enable_text_shaping(self, value: bool):
    ...

```

### Remarks

Text shaping is only performed when exporting to PDF or XPS formats.
For Windows platforms no additional efforts are required because Aspose.Words for Python via Net already includes compiled `HarfBuzz` library.
For other systems, Aspose.Words for Python via Net relies on already installed `HarfBuzz` library.
For instance, many Linux-based systems have `HarfBuzz` installed system-wide by default.
If not, there is usually a package available for installing via package manager.


### Examples

Shows how to use enable_text_shaping property.

```python
doc =  aw.Document(file_name=MY_DIR + "TestMetricsKerning.docx")
doc.layout_options.enable_text_shaping = True
doc.save( file_name=ARTIFACTS_DIR + 'out_HarfBuzz.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

