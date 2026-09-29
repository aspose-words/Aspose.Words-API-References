---
title: PdfSaveOptions constructor
linktitle: PdfSaveOptions constructor
articleTitle: PdfSaveOptions constructor
second_title: Aspose.Words for Python
description: "PdfSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../../aspose.words/saveformat/#PDF) format."
type: docs
weight: 10
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/__init__/
---

## PdfSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the
[SaveFormat.PDF](../../../aspose.words/saveformat/#PDF) format.



```python
def __init__(self):
    ...
```

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

