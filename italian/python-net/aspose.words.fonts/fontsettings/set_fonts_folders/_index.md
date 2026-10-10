---
title: FontSettings.set_fonts_folders method
linktitle: set_fonts_folders method
articleTitle: set_fonts_folders method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folders method. Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts."
type: docs
weight: 90
url: /it/python-net/aspose.words.fonts/fontsettings/set_fonts_folders/
---

## set_fonts_folders(fonts_folders, recursive) {#strlist_bool}

Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.


```python
def set_fonts_folders(self, fonts_folders: List[str], recursive: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| fonts_folders | List[str] | An array of folders that contain TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

### Remarks

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




### Examples

Shows how to set multiple font source directories.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
builder.font.name = 'Junction Light'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Le nostre font source non contengono il font che abbiamo usato per il testo in questo documento.
# Se utilizziamo queste impostazioni dei font durante il rendering di questo documento,
# Aspose.Words applicherà un font di riserva al testo che ha un font che Aspose.Words non riesce a trovare.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# Le font source predefinite non contengono i due font che stiamo usando in questo documento.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# Utilizza il metodo "SetFontsFolders" per creare una sorgente di caratteri da ogni directory di font che passiamo come primo argomento.
# Passa "false" come argomento "recursive" per includere i caratteri da tutti i file di font presenti nelle directory
# che stiamo passando come primo argomento, ma non includere alcun carattere dalle sottocartelle delle directory.
# Passa "true" come argomento "recursive" per includere tutti i file di font nelle directory che stiamo passando
# nel primo argomento, così come tutti i caratteri nelle loro sottodirectory.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + '/Amethysta', FONTS_DIR + '/Junction'], recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(2, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
# La cartella "Junction" stessa non contiene file di caratteri, ma ha sottocartelle che li contengono.
if recursive:
    self.assertEqual(11, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Junction Light' for f in new_font_sources[1].get_available_fonts()]))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolders.pdf')
# Ripristina le font source originali.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

