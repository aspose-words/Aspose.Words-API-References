---
title: FontSettings class
linktitle: FontSettings class
articleTitle: FontSettings class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSettings class. Specifies font settings for a document"
type: docs
weight: 160
url: /de/python-net/aspose.words.fonts/fontsettings/
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
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arvo'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Unsere Schriftquellen enthalten nicht die Schrift, die wir für den Text in diesem Dokument verwendet haben.
# Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
# wird Aspose.Words eine Ersatzschrift auf Text anwenden, dessen Schrift von Aspose.Words nicht gefunden werden kann.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# In den Standard-Schriftquellen fehlen die beiden Schriften, die wir in diesem Dokument verwenden.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
# Verwenden Sie die Methode "SetFontsFolder", um ein Verzeichnis festzulegen, das als neue Schriftquelle dient.
# Übergeben Sie "false" als "recursive"-Argument, um Schriften aus allen Schriftdateien im Verzeichnis einzuschließen
# die wir im ersten Argument übergeben, jedoch keine Schriften in Unterordnern dieses Verzeichnisses einbeziehen.
# Übergeben Sie "true" als "recursive"-Argument, um alle Schriftdateien im Verzeichnis, das wir übergeben, einzuschließen
# im ersten Argument, sowie alle Schriften in dessen Unterverzeichnissen.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in new_font_sources[0].get_available_fonts()]))
# Die Schrift "Amethysta" befindet sich in einem Unterordner des Schriftverzeichnisses.
if recursive:
    self.assertEqual(30, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolder.pdf')
# Stellen Sie die ursprünglichen Schriftquellen wieder her.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

Shows how to set multiple font source directories.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Unsere Schriftquellen enthalten nicht die Schrift, die wir für den Text in diesem Dokument verwendet haben.
# Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
# wird Aspose.Words eine Ersatzschrift auf Text anwenden, dessen Schrift von Aspose.Words nicht gefunden werden kann.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# In den Standard-Schriftquellen fehlen die beiden Schriften, die wir in diesem Dokument verwenden.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# Verwenden Sie die Methode "SetFontsFolders", um eine Schriftquelle aus jedem Schriftverzeichnis zu erstellen, das wir als erstes Argument übergeben.
# Übergeben Sie "false" als das "recursive"-Argument, um Schriften aus allen Schriftdateien einzuschließen, die sich in den Verzeichnissen befinden.
# die wir als erstes Argument übergeben, aber keine Schriften aus den Unterordnern der Verzeichnisse einbeziehen.
# Übergeben Sie "true" als das "recursive"-Argument, um alle Schriftdateien in den Verzeichnissen einzuschließen, die wir übergeben.
# im ersten Argument, sowie alle Schriften in deren Unterverzeichnissen.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + '/Amethysta', FONTS_DIR + '/Junction'], recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(2, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
# Der Ordner "Junction" selbst enthält keine Schriftdateien, hat aber Unterordner, die welche enthalten.
if recursive:
    self.assertEqual(11, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Junction Light' for f in new_font_sources[1].get_available_fonts()]))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolders.pdf')
# Stellen Sie die ursprünglichen Schriftquellen wieder her.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

Shows how to add a font source to our existing font sources.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# Der Standard‑Schriftquelle fehlen zwei der Schriften, die wir in unserem Dokument verwenden.
# Wenn wir dieses Dokument speichern, wird Aspose.Words Ersatzschriften auf allen Text anwenden, der mit nicht zugänglichen Schriften formatiert ist.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# Erstellen Sie eine Schriftquelle aus einem Ordner, der Schriften enthält.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
# Wenden Sie ein neues Array von Schriftquellen an, das die ursprünglichen Schriftquellen sowie unsere benutzerdefinierten Schriften enthält.
updated_font_sources = [original_font_sources[0], folder_font_source]
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=updated_font_sources)
# Verifizieren Sie, dass Aspose.Words Zugriff auf alle erforderlichen Schriften hat, bevor wir das Dokument zu PDF rendern.
updated_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in updated_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in updated_font_sources[1].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Junction Light' for f in updated_font_sources[1].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.AddFontSource.pdf')
# Stellen Sie die ursprünglichen Schriftquellen wieder her.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../)

