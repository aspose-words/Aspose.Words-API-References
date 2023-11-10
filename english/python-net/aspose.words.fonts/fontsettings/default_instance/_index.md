---
title: FontSettings.default_instance property
linktitle: default_instance property
articleTitle: default_instance property
second_title: Aspose.Words for Python
description: "FontSettings.default_instance property. Static default font settings."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/fontsettings/default_instance/
---

## FontSettings.default_instance property

Static default font settings.


```python
@property
def default_instance(self) -> aspose.words.fonts.FontSettings:
    ...

```

### Remarks

This instance is used by default in a document unless [Document.font_settings](../../../aspose.words/document/font_settings/) is specified.



### Examples

Shows how to configure the default font settings instance.

```python
# Configure the default font settings instance to use the "Courier New" font
# as a backup substitute when we attempt to use an unknown font.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = "Courier New"

self.assertTrue(aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.enabled)

doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Non-existent font"
builder.write("Hello world!")

# This document does not have a FontSettings configuration. When we render the document,
# the default "font_settings" instance will resolve the missing font.
# Aspose.Words will use "Courier New" to render text that uses the unknown font.
self.assertIsNone(doc.font_settings)

doc.save(ARTIFACTS_DIR + "FontSettings.default_font_instance.pdf")
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

