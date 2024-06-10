---
title: FontFallbackSettings.build_automatic method
linktitle: build_automatic method
articleTitle: build_automatic method
second_title: Aspose.Words for Python
description: "FontFallbackSettings.build_automatic method. Automatically builds the fallback settings by scanning available fonts."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/fontfallbacksettings/build_automatic/
---

## build_automatic() {#default}

Automatically builds the fallback settings by scanning available fonts.


```python
def build_automatic(self):
    ...
```

### Remarks

This method may produce non-optimal fallback settings. Fonts are checked by [
            Unicode Character Range](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) fields and not by the actual glyphs presence. Also Unicode ranges are checked individually 
and several ranges related to single language/script may use different fallback fonts.



### Examples

Shows how to distribute fallback fonts across Unicode character code ranges.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
font_fallback_settings = font_settings.fallback_settings
# Configure our font settings to source fonts only from the "MyFonts" folder.
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, False)
font_settings.set_fonts_sources([folder_font_source])
# Calling the "build_automatic" method will generate a fallback scheme that
# distributes accessible fonts across as many Unicode character codes as possible.
# In our case, it only has access to the handful of fonts inside the "MyFonts" folder.
font_fallback_settings.build_automatic()
font_fallback_settings.save(ARTIFACTS_DIR + 'FontSettings.fallback_settings_custom.build_automatic.xml')
# We can also load a custom substitution scheme from a file like this.
# This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
# and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
font_fallback_settings.load(MY_DIR + 'Custom font fallback settings.xml')
# Create a document builder and set its font to one that does not exist in any of our sources.
# Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Missing Font'
# Use the builder to print every Unicode character from 0x0021 to 0x052F,
# with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
for i in range(33, 1328):
    if i == 33:
        builder.writeln('\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in "AllegroOpen" font:')
    elif i == 256:
        builder.writeln('\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in "AllegroOpen" font:')
    elif i == 592:
        builder.writeln('\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in "M+ 2m" font:')
    builder.write(chr(i))
doc.save(ARTIFACTS_DIR + 'FontSettings.fallback_settings_custom.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontFallbackSettings](../)

