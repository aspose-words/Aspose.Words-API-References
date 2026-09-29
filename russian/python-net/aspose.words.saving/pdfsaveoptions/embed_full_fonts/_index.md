---
title: PdfSaveOptions.embed_full_fonts property
linktitle: embed_full_fonts property
articleTitle: embed_full_fonts property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.embed_full_fonts property. Controls how fonts are embedded into the resulting PDF documents."
type: docs
weight: 120
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/embed_full_fonts/
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
# Настройте наши источники шрифтов, чтобы обеспечить доступ к обоим шрифтам в этом документе.
original_fonts_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=[original_fonts_sources[0], folder_font_source])
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in font_sources[1].get_available_fonts()]))
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Поскольку наш документ содержит пользовательский шрифт, внедрение его в выходной документ может быть желательным.
# Установите свойство "EmbedFullFonts" в значение "true", чтобы внедрить каждый глиф каждого встроенного шрифта в выходной PDF.
# Размер документа может стать очень большим, но мы получим полный доступ ко всем шрифтам, если будем редактировать PDF.
# Установите свойство "EmbedFullFonts" в значение "false", чтобы применить субсетинг к шрифтам, сохраняя только глифы
# которые использует документ. Файл будет значительно меньше,
# но нам может потребоваться доступ к любым пользовательским шрифтам, если мы будем редактировать документ.
options.embed_full_fonts = embed_full_fonts
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedFullFonts.pdf', save_options=options)
# Восстановите оригинальные источники шрифтов.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_fonts_sources)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

