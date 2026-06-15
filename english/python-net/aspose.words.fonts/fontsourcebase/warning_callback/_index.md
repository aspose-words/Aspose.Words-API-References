---
title: FontSourceBase.warning_callback property
linktitle: warning_callback property
articleTitle: warning_callback property
second_title: Aspose.Words for Python
description: "FontSourceBase.warning_callback property. Called during processing of font source when an issue is detected that might result in formatting fidelity loss."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/fontsourcebase/warning_callback/
---

## FontSourceBase.warning_callback property

Called during processing of font source when an issue is detected that might result in formatting fidelity loss.


```python
@property
def warning_callback(self) -> aspose.words.IWarningCallback:
    ...

@warning_callback.setter
def warning_callback(self, value: aspose.words.IWarningCallback):
    ...

```

### Examples

Shows how to call warning callback when the font sources working with.

```python
settings = aw.fonts.FontSettings()
settings.set_fonts_folder('bad folder?', False)
source = settings.get_fonts_sources()[0]
callback = self.FontSourceWarningCollector()
source.warning_callback = callback
# Get the list of fonts to call warning callback.
font_infos = source.get_available_fonts()
self.assertTrue('Error loading font from the folder "bad folder?"' in callback.font_substitution_warnings[0].description)
```

Shows how to call warning callback when the font sources working with (FontSourceWarningCollector).

```python
class FontSourceWarningCollector(aw.IWarningCallback):

    def __init__(self):
        self.font_substitution_warnings = aw.WarningInfoCollection()

    def warning(self, info):
        self.font_substitution_warnings.warning(info)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSourceBase](../)

