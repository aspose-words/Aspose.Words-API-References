---
title: set_fonts_sources method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.fonts.FontSettings.set_fonts_sources method"
type: docs
weight: 100
url: /python-net/aspose.words.fonts/fontsettings/set_fonts_sources/
---

## set_fonts_sources(sources) {#fontsourcebaselist}

Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.


```python
def set_fonts_sources(self, sources: List[aspose.words.fonts.FontSourceBase]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| sources | List[[FontSourceBase](../../fontsourcebase/)] |  |

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




## set_fonts_sources(sources, cache_input_stream) {#fontsourcebaselist_bytesio}

Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved
font search cache.


```python
def set_fonts_sources(self, sources: List[aspose.words.fonts.FontSourceBase], cache_input_stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| sources | List[[FontSourceBase](../../fontsourcebase/)] |  |
| cache_input_stream | BytesIO |  |

Loading previously saved font search cache will speed up the font cache initialization process. It is
especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

When saving and loading font search cache, fonts in the provided sources are identified via cache key.
For the fonts in the [SystemFontSource](../../systemfontsource/) and [FolderFontSource](../../folderfontsource/) cache key is the path
to the font file. For [MemoryFontSource](../../memoryfontsource/) and [StreamFontSource](../../streamfontsource/) cache key is defined
in the [MemoryFontSource.cache_key](../../memoryfontsource/cache_key/) and [StreamFontSource.cache_key](../../streamfontsource/cache_key/) properties
respectively. For the [FileFontSource](../../filefontsource/) cache key is either [FileFontSource.cache_key](../../filefontsource/cache_key/)
property or a file path if the [FileFontSource.cache_key](../../filefontsource/cache_key/) is **null**.

It is highly recommended to provide the same font sources when loading cache as at the time the cache was saved.
Any changes in the font sources (e.g. adding new fonts, moving font files or changing the cache key) may lead to the
inaccurate font resolving by Aspose.Words.




## Examples

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

## See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

