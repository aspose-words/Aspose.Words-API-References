---
title: FontFallbackSettings class
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies font fallback mechanism settings"
type: docs
weight: 70
url: /python-net/aspose.words.fonts/fontfallbacksettings/
---

## FontFallbackSettings class

Specifies font fallback mechanism settings.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




By default fallback settings are initialized with predefined settings which mimics the Microsoft Word fallback.


### Methods

| Name | Description |
| --- | --- |
|[ build_automatic()](./build_automatic/#default) | Automatically builds the fallback settings by scanning available fonts. |
|[ load(file_name)](./load/#str) | Loads font fallback settings from XML file. |
|[ load(stream)](./load/#bytesio) | Loads fallback settings from XML stream. |
|[ load_ms_office_fallback_settings()](./load_ms_office_fallback_settings/#default) | Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts. |
|[ load_noto_fallback_settings()](./load_noto_fallback_settings/#default) | Loads predefined fallback settings which uses Google Noto fonts. |
|[ save(output_stream)](./save/#bytesio) | Saves the current fallback settings to stream. |
|[ save(file_name)](./save/#str) | Saves the current fallback settings to file. |

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
font_fallback_settings.save(ARTIFACTS_DIR + "FontSettings.fallback_settings_custom.build_automatic.xml")

# We can also load a custom substitution scheme from a file like this.
# This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
# and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
font_fallback_settings.load(MY_DIR + "Custom font fallback settings.xml")

# Create a document builder and set its font to one that does not exist in any of our sources.
# Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
builder = aw.DocumentBuilder(doc)
builder.font.name = "Missing Font"

# Use the builder to print every Unicode character from 0x0021 to 0x052F,
# with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
for i in range(0x0021, 0x0530):
    if i == 0x0021:
        builder.writeln("\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:")
    elif i == 0x0100:
        builder.writeln("\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:")
    elif i == 0x0250:
        builder.writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:")

    builder.write(chr(i))

doc.save(ARTIFACTS_DIR + "FontSettings.fallback_settings_custom.pdf")
```

### See Also

* module [aspose.words.fonts](../)

