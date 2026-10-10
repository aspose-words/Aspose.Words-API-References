---
title: FontSettings.set_fonts_folder method
linktitle: set_fonts_folder method
articleTitle: set_fonts_folder method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folder method. Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts"
type: docs
weight: 80
url: /ru/python-net/aspose.words.fonts/fontsettings/set_fonts_folder/
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
# Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
# Если мы используем эти настройки шрифтов при рендеринге этого документа,
# Aspose.Words применит резервный шрифт к тексту, у которого шрифт не может быть найден Aspose.Words.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
# Используйте метод "SetFontsFolder", чтобы задать каталог, который будет выступать в качестве нового источника шрифтов.
# Передайте "false" в качестве аргумента "recursive", чтобы включить шрифты из всех файлов шрифтов, находящихся в каталоге
# которые мы передаем в первом аргументе, но не включать шрифты из подпапок этого каталога.
# Передайте "true" в качестве аргумента "recursive", чтобы включить все файлы шрифтов в каталоге, который мы передаем
# в первом аргументе, а также все шрифты в его подпапках.
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in new_font_sources[0].get_available_fonts()]))
# Шрифт "Amethysta" находится в подпапке каталога шрифтов.
if recursive:
    self.assertEqual(30, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolder.pdf')
# Восстановите оригинальные источники шрифтов.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

