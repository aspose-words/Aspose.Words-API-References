---
title: FontSettings class
linktitle: FontSettings class
articleTitle: FontSettings class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSettings class. Specifies font settings for a document"
type: docs
weight: 140
url: /python-net/aspose.words.fonts/fontsettings/
---

## FontSettings class

Specifies font settings for a document.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Remarks

Aspose.Words uses font settings to resolve the fonts in the document. Fonts are resolved mostly when building document layout
or rendering to fixed page formats. But when loading some formats, Aspose.Words also may require to resolve the fonts. For example, when
loading HTML documents Aspose.Words may resolve the fonts to perform font fallback. So it is recommended that you set the font settings in
[LoadOptions](../../aspose.words.loading/loadoptions/) when loading the document. Or at least before building the layout or rendering the document to the fixed-page format.

By default all documents uses single static font settings instance. It could be accessed by
[FontSettings.default_instance](./default_instance/) property.

Changing font settings is safe at any time from any thread. But it is recommended that you do not change the font settings while
processing some documents which uses this settings. This can lead to the fact that the same font will be resolved differently
in different parts of the document.




### Constructors
| Name | Description |
| --- | --- |
| [FontSettings()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [default_instance](./default_instance/) | Static default font settings. |
| [fallback_settings](./fallback_settings/) | Settings related to font fallback mechanism. |
| [substitution_settings](./substitution_settings/) | Settings related to font substitution mechanism. |

### Methods

| Name | Description |
| --- | --- |
|[ get_fonts_sources()](./get_fonts_sources/#default) | Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts. |
|[ reset_font_sources()](./reset_font_sources/#default) | Resets the fonts sources to the system default. |
|[ save_search_cache(output_stream)](./save_search_cache/#bytesio) | Saves the font search cache to the stream. |
|[ set_fonts_folder(font_folder, recursive)](./set_fonts_folder/#str_bool) | Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to [FontSettings.set_fonts_folders()](./set_fonts_folders/#strlist_bool) for setting only one font directory. |
|[ set_fonts_folders(fonts_folders, recursive)](./set_fonts_folders/#strlist_bool) | Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
|[ set_fonts_sources(sources)](./set_fonts_sources/#fontsourcebaselist) | Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
|[ set_fonts_sources(sources, cache_input_stream)](./set_fonts_sources/#fontsourcebaselist_bytesio) | Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved font search cache. |

### Examples

Shows how to set a font source directory.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Arvo"
builder.writeln("Hello world!")
builder.font.name = "Amethysta"
builder.writeln("The quick brown fox jumps over the lazy dog.")

# Our font sources do not contain the font that we have used for text in this document.
# If we use these font settings while rendering this document,
# Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(original_font_sources))
self.assertTrue(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))

# The default font sources are missing the two fonts that we are using in this document.
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arvo"))
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))

# Use the "set_fonts_folder" method to set a directory which will act as a new font source.
# Pass "False" as the "recursive" argument to include fonts from all the font files that are in the directory
# that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
# Pass "True" as the "recursive" argument to include all font files in the directory that we are passing
# in the first argument, as well as all the fonts in its subdirectories.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)

new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(new_font_sources))
self.assertFalse(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))
self.assertTrue(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Arvo"))

# The "Amethysta" font is in a subfolder of the font directory.
if recursive:
    self.assertEqual(25, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))

doc.save(ARTIFACTS_DIR + "FontSettings.set_fonts_folder.pdf")

# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(original_font_sources)
```

Shows how to set multiple font source directories.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Amethysta"
builder.writeln("The quick brown fox jumps over the lazy dog.")
builder.font.name = "Junction Light"
builder.writeln("The quick brown fox jumps over the lazy dog.")

# Our font sources do not contain the font that we have used for text in this document.
# If we use these font settings while rendering this document,
# Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(1, len(original_font_sources))
self.assertTrue(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))

# The default font sources are missing the two fonts that we are using in this document.
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))
self.assertFalse(any(f for f in original_font_sources[0].get_available_fonts() if f.full_font_name == "Junction Light"))

# Use the "set_fonts_folders" method to create a font source from each font directory that we pass as the first argument.
# Pass "False" as the "recursive" argument to include fonts from all the font files that are in the directories
# that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
# Pass "True" as the "recursive" argument to include all font files in the directories that we are passing
# in the first argument, as well as all the fonts in their subdirectories.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + "/Amethysta", FONTS_DIR + "/Junction"], recursive)

new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

self.assertEqual(2, len(new_font_sources))
self.assertFalse(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any(f for f in new_font_sources[0].get_available_fonts() if f.full_font_name == "Amethysta"))

# The "Junction" folder itself contains no font files, but has subfolders that do.
if recursive:
    self.assertEqual(6, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any(f for f in new_font_sources[1].get_available_fonts() if f.full_font_name == "Junction Light"))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))

doc.save(ARTIFACTS_DIR + "FontSettings.set_fonts_folders.pdf")

# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(original_font_sources)
```

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

* module [aspose.words.fonts](../)

