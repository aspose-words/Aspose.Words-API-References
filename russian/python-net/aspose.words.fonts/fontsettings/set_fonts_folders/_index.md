---
title: FontSettings.set_fonts_folders method
linktitle: set_fonts_folders method
articleTitle: set_fonts_folders method
second_title: Aspose.Words for Python
description: "FontSettings.set_fonts_folders method. Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts."
type: docs
weight: 90
url: /ru/python-net/aspose.words.fonts/fontsettings/set_fonts_folders/
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
# Наши источники шрифтов не содержат шрифт, который мы использовали для текста в этом документе.
# Если мы используем эти настройки шрифтов при рендеринге этого документа,
# Aspose.Words применит резервный шрифт к тексту, у которого шрифт не может быть найден Aspose.Words.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# В источниках шрифтов по умолчанию отсутствуют два шрифта, которые мы используем в этом документе.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# Используйте метод "SetFontsFolders", чтобы создать источник шрифтов из каждой папки шрифтов, которую мы передаем в качестве первого аргумента.
# Передайте "false" в качестве аргумента "recursive", чтобы включить шрифты из всех файлов шрифтов, находящихся в каталогах.
# которые мы передаем в первом аргументе, но не включать шрифты из подпапок любых каталогов.
# Передайте "true" в качестве аргумента "recursive", чтобы включить все файлы шрифтов в каталогах, которые мы передаем.
# в первом аргументе, а также все шрифты в их подпапках.
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + '/Amethysta', FONTS_DIR + '/Junction'], recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(2, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
# Папка "Junction" сама по себе не содержит файлов шрифтов, но имеет подпапки, в которых они есть.
if recursive:
    self.assertEqual(11, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Junction Light' for f in new_font_sources[1].get_available_fonts()]))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolders.pdf')
# Восстановите оригинальные источники шрифтов.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

