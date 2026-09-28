---
title: FontSettings class
linktitle: FontSettings class
articleTitle: FontSettings class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSettings class. Specifies font settings for a document"
type: docs
weight: 160
url: /zh/python-net/aspose.words.fonts/fontsettings/
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
# 我们的字体源不包含我们在此文档中用于文本的字体。
# 如果在渲染此文档时使用这些字体设置，
# Aspose.Words 将对使用了 Aspose.Words 无法定位的字体的文本应用回退字体。
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# 默认字体源缺少我们在此文档中使用的两种字体。
self.assertFalse(any([f.full_font_name == 'Arvo' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
# 使用 "SetFontsFolder" 方法设置一个目录，该目录将作为新的字体源。
# 将 "false" 作为 "recursive" 参数传入，以包含目录中所有字体文件的字体
# 我们在第一个参数中传入的目录，但不包括该目录任何子文件夹中的字体。
# 将 "true" 作为 "recursive" 参数传入，以包含我们传入的目录中的所有字体文件
# 在第一个参数中，以及其子目录中的所有字体。
aw.fonts.FontSettings.default_instance.set_fonts_folder(FONTS_DIR, recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in new_font_sources[0].get_available_fonts()]))
# “Amethysta” 字体位于字体目录的子文件夹中。
if recursive:
    self.assertEqual(30, len(new_font_sources[0].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
else:
    self.assertEqual(18, len(new_font_sources[0].get_available_fonts()))
    self.assertFalse(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolder.pdf')
# 恢复原始字体源。
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
# 我们的字体源不包含我们在此文档中用于文本的字体。
# 如果在渲染此文档时使用这些字体设置，
# Aspose.Words 将对使用了 Aspose.Words 无法定位的字体的文本应用回退字体。
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(1, len(original_font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in original_font_sources[0].get_available_fonts()]))
# 默认字体源缺少我们在此文档中使用的两种字体。
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# 使用 "SetFontsFolders" 方法从我们作为第一个参数传入的每个字体目录创建字体源。
# 将 "false" 作为 "recursive" 参数传递，以包含目录中所有字体文件的字体
# 我们在第一个参数中传入的，但不包括任何目录子文件夹中的字体。
# 将 "true" 作为 "recursive" 参数传递，以包含我们传入的目录中的所有字体文件
# 在第一个参数中，以及它们子目录中的所有字体。
aw.fonts.FontSettings.default_instance.set_fonts_folders([FONTS_DIR + '/Amethysta', FONTS_DIR + '/Junction'], recursive)
new_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertEqual(2, len(new_font_sources))
self.assertFalse(any([f.full_font_name == 'Arial' for f in new_font_sources[0].get_available_fonts()]))
self.assertEqual(1, len(new_font_sources[0].get_available_fonts()))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in new_font_sources[0].get_available_fonts()]))
# "Junction" 文件夹本身不包含字体文件，但其子文件夹中有。
if recursive:
    self.assertEqual(11, len(new_font_sources[1].get_available_fonts()))
    self.assertTrue(any([f.full_font_name == 'Junction Light' for f in new_font_sources[1].get_available_fonts()]))
else:
    self.assertEqual(0, len(new_font_sources[1].get_available_fonts()))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SetFontsFolders.pdf')
# 恢复原始字体源。
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
# 默认字体源缺少我们文档中使用的两个字体。
# 当我们保存此文档时，Aspose.Words 将对所有使用不可访问字体格式化的文本应用回退字体。
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in original_font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Junction Light' for f in original_font_sources[0].get_available_fonts()]))
# 从包含字体的文件夹创建字体源。
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
# 应用一个新的字体源数组，其中包含原始字体源以及我们的自定义字体。
updated_font_sources = [original_font_sources[0], folder_font_source]
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=updated_font_sources)
# 在将文档渲染为 PDF 之前，验证 Aspose.Words 是否能够访问所有必需的字体。
updated_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in updated_font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Amethysta' for f in updated_font_sources[1].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Junction Light' for f in updated_font_sources[1].get_available_fonts()]))
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.AddFontSource.pdf')
# 恢复原始字体源。
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
```

### See Also

* module [aspose.words.fonts](../)

