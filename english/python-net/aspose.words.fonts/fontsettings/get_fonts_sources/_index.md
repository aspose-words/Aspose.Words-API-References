---
title: get_fonts_sources method
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts."
type: docs
weight: 50
url: /python-net/aspose.words.fonts/fontsettings/get_fonts_sources/
---

## get_fonts_sources() {#default}

Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.


```python
def get_fonts_sources(self):
    ...
```

The returned value is a copy of the data that Aspose.Words uses. If you change the entries
in the returned array, it will have no effect on document rendering. To specify new font sources
use the [FontSettings.set_fonts_sources()](../set_fonts_sources/#fontsourcebaselist) method.




### Returns

A copy of the current font sources.


### Examples

Shows how to add a font source to our existing font sources.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Arial"
builder.writeln("Hello world!")
builder.font.name = "Amethysta"
builder.writeln("The quick brown fox jumps over the lazy dog.")
builder.font.name = "Junction Light"
builder.writeln("The quick brown fox jumps over the lazy dog.")

original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(original_font_sources))

self.assertTrue(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))

# The default font source is missing two of the fonts that we are using in our document.
# When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Junction Light"))

# Create a font source from a folder that contains fonts.
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, True)

# Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
updated_font_sources = [original_font_sources[0], folder_font_source]
aw.fonts.FontSettings.default_instance.set_fonts_sources(updated_font_sources)

# Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
updated_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertTrue(any(f for f in updated_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))
self.assertTrue(any(f for f in updated_font_sources[1].get_available_fonts() if f.full_font_name == "Amethysta"))
self.assertTrue(any(f for f in updated_font_sources[1].get_available_fonts() if f.full_font_name == "Junction Light"))

doc.save(ARTIFACTS_DIR + "FontSettings.add_font_source.pdf")

# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

