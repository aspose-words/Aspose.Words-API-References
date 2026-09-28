---
title: PdfSaveOptions.embed_full_fonts property
linktitle: embed_full_fonts property
articleTitle: embed_full_fonts property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.embed_full_fonts property. Controls how fonts are embedded into the resulting PDF documents."
type: docs
weight: 120
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/embed_full_fonts/
---

## PdfSaveOptions.embed_full_fonts property

Controls how fonts are embedded into the resulting PDF documents.


```python
@property
def embed_full_fonts(self) -> bool:
    ...

@embed_full_fonts.setter
def embed_full_fonts(self, value: bool):
    ...

```

### Remarks

The default value is ``False``, which means the fonts are subsetted before embedding.
Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all
unused glyphs from a font.

When this value is set to ``True``, a complete font file is embedded into PDF without
subsetting. This will result in larger output files, but can be a useful option when you want to
edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting
will result in large output documents.




### Examples

Shows how to enable or disable subsetting when embedding fonts while rendering a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Arvo'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# 配置我们的字体来源，以确保能够访问此文档中的两种字体。
original_fonts_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=[original_fonts_sources[0], folder_font_source])
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in font_sources[1].get_available_fonts()]))
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 由于文档包含自定义字体，嵌入到输出文档中可能是可取的。
# 将 "EmbedFullFonts" 属性设置为 "true"，以在输出的 PDF 中嵌入每个已嵌入字体的所有字形。
# 文档大小可能会变得非常大，但如果我们编辑 PDF，将可以完整使用所有字体。
# 将 "EmbedFullFonts" 属性设置为 "false" 以对字体进行子集化，仅保存使用的字形
# 文档实际使用的字形。文件将显著变小，
# 但如果我们编辑文档，可能需要访问任何自定义字体。
options.embed_full_fonts = embed_full_fonts
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedFullFonts.pdf', save_options=options)
# 恢复原始字体源。
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_fonts_sources)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

