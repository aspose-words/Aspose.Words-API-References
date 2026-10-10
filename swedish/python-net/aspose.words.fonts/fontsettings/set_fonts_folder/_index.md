---
title: FontSettings.set_fonts_folder method
linktitle: set_fonts_folder method
articleTitle: set_fonts_folder method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folder method. Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts"
type: docs
weight: 80
url: /sv/python-net/aspose.words.fonts/fontsettings/set_fonts_folder/
---

## set_fonts_folder(font_folder, recursive) {#str_bool}

Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.
This is a shortcut to [FontSettings.set_fonts_folders()](../set_fonts_folders/#strlist_bool) for setting only one font directory.



```python
def set_fonts_folder(self, font_folder: str, recursive: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_folder | str | The folder that contains TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

### Examples

Shows how to set a font source directory.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arvo'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Våra teckensnittskällor innehåller inte det teckensnitt som vi har använt för text i detta dokument.
# Om vi använder dessa teckensnittinställningar när vi renderar detta dokument,
# Aspose.Words kommer att tillämpa ett reservteckensnitt på text som har ett teckensnitt som Aspose.Words inte kan hitta.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# Standardteckensnittskällorna saknar de två teckensnitten som vi använder i detta dokument.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
# Använd metoden "SetFontsFolder" för att ange en katalog som kommer att fungera som en ny teckensnittskälla.
# Skicka "false" som argumentet "recursive" för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogen
# som vi skickar som första argument, men inkludera inte några teckensnitt i någon av katalogens undermappar.
# Skicka "true" som argumentet "recursive" för att inkludera alla teckensnittsfiler i katalogen som vi skickar
# i det första argumentet, samt alla teckensnitt i dess underkataloger.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in new_font_sources[0].get_available_fonts()]))
# Teckensnittet "Amethysta" finns i en undermapp till teckensnittskatalogen.
if recursive:
    self.assertEqual(30, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolder.pdf')
# Återställ de ursprungliga teckensnittskällorna.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

