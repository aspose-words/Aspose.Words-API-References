---
title: FontSettings.set_fonts_sources method
linktitle: set_fonts_sources method
articleTitle: set_fonts_sources method
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSettings.set_fonts_sources method"
type: docs
weight: 100
url: /zh/python-net/aspose.words.fonts/fontsettings/set_fonts_sources/
---

## set_fonts_sources(sources) {#fontsourcebaselist}

Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.


```python
def set_fonts_sources(self, sources: List[aspose.words.fonts.FontSourceBase]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| sources | List[[FontSourceBase](../../fontsourcebase/)] | An array of sources that contain TrueType fonts. |

### Remarks

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




## set_fonts_sources(sources, cache_input_stream) {#fontsourcebaselist_bytesio}

Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved
font search cache.


```python
def set_fonts_sources(self, sources: List[aspose.words.fonts.FontSourceBase], cache_input_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| sources | List[[FontSourceBase](../../fontsourcebase/)] | An array of sources that contain TrueType fonts. |
| cache_input_stream | io.BytesIO | Input stream with saved font search cache. |

### Remarks

Loading previously saved font search cache will speed up the font cache initialization process. It is
especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

When saving and loading font search cache, fonts in the provided sources are identified via cache key.
For the fonts in the [SystemFontSource](../../systemfontsource/) and [FolderFontSource](../../folderfontsource/) cache key is the path
to the font file. For [MemoryFontSource](../../memoryfontsource/) and [StreamFontSource](../../streamfontsource/) cache key is defined
in the [MemoryFontSource.cache_key](../../memoryfontsource/cache_key/) and [StreamFontSource.cache_key](../../streamfontsource/cache_key/) properties
respectively. For the [FileFontSource](../../filefontsource/) cache key is either [FileFontSource.cache_key](../../filefontsource/cache_key/)
property or a file path if the [FileFontSource.cache_key](../../filefontsource/cache_key/) is ``None``.

It is highly recommended to provide the same font sources when loading cache as at the time the cache was saved.
Any changes in the font sources (e.g. adding new fonts, moving font files or changing the cache key) may lead to the
inaccurate font resolving by Aspose.Words.




## Examples

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

## See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

