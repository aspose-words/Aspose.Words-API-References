---
title: load_noto_fallback_settings method
second_title: Aspose.Words for Python via .NET API Reference
description: "Loads predefined fallback settings which uses Google Noto fonts."
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

# These are free fonts licensed under the SIL Open Font License.
# We can download the fonts here:
# https://www.google.com/get/noto/#sans-lgc
font_settings.set_fonts_folder(FONTS_DIR + "Noto", False)

# Note that the predefined settings only use Sans-style Noto fonts with regular weight.
# Some of the Noto fonts use advanced typography features.
# Fonts featuring advanced typography may not be rendered correctly as Aspose.Words currently do not support them.
font_settings.fallback_settings.load_noto_fallback_settings()
font_settings.substitution_settings.font_info_substitution.enabled = False
font_settings.substitution_settings.default_font_substitution.default_font_name = "Noto Sans"

doc = aw.Document()
doc.font_settings = font_settings
```

Shows how to load pre-defined fallback font settings.

```python
doc = aw.Document()

font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
font_fallback_settings = font_settings.fallback_settings

# Save the default fallback font scheme to an XML document.
# For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
# This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
# the fallback scheme will use symbols from the "Vani" font substitute.
font_fallback_settings.save(ARTIFACTS_DIR + "FontSettings.fallback_settings.default.xml")

# Below are two pre-defined font fallback schemes we can choose from.
# 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
font_fallback_settings.load_ms_office_fallback_settings()
font_fallback_settings.save(ARTIFACTS_DIR + "FontSettings.fallback_settings.load_ms_office_fallback_settings.xml")

# 2 -  Use the scheme built from Google Noto fonts:
font_fallback_settings.load_noto_fallback_settings()
font_fallback_settings.save(ARTIFACTS_DIR + "FontSettings.fallback_settings.load_noto_fallback_settings.xml")
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

