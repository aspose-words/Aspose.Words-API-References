---
title: FontFallbackSettings.load_noto_fallback_settings method
linktitle: load_noto_fallback_settings method
articleTitle: load_noto_fallback_settings method
second_title: Aspose.Words for Python
description: "FontFallbackSettings.load_noto_fallback_settings method. Loads predefined fallback settings which uses Google Noto fonts."
type: docs
weight: 40
url: /python-net/aspose.words.fonts/fontfallbacksettings/load_noto_fallback_settings/
---

## load_noto_fallback_settings() {#default}

Loads predefined fallback settings which uses Google Noto fonts.


```python
def load_noto_fallback_settings(self):
    ...
```

### Examples

Shows how to add predefined font fallback settings for Google Noto fonts.

```python
font_settings = aw.fonts.FontSettings()
font_settings.set_fonts_folder(FONTS_DIR + 'Noto', False)
font_settings.fallback_settings.load_noto_fallback_settings()
font_settings.substitution_settings.font_info_substitution.enabled = False
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Noto Sans'
doc = aw.Document()
doc.font_settings = font_settings
```

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

