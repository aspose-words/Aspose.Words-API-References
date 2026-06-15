---
title: FontFallbackSettings.load_ms_office_fallback_settings method
linktitle: load_ms_office_fallback_settings method
articleTitle: load_ms_office_fallback_settings method
second_title: Aspose.Words for Python
description: "FontFallbackSettings.load_ms_office_fallback_settings method. Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/fontfallbacksettings/load_ms_office_fallback_settings/
---

## load_ms_office_fallback_settings() {#default}

Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts.


```python
def load_ms_office_fallback_settings(self):
    ...
```

### Examples

Shows how to load pre-defined fallback font settings.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
font_fallback_settings = font_settings.fallback_settings
font_fallback_settings.save(file_name=ARTIFACTS_DIR + 'FontSettings.FallbackSettings.Default.xml')
font_fallback_settings.load_ms_office_fallback_settings()
font_fallback_settings.save(file_name=ARTIFACTS_DIR + 'FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml')
font_fallback_settings.load_noto_fallback_settings()
font_fallback_settings.save(file_name=ARTIFACTS_DIR + 'FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

