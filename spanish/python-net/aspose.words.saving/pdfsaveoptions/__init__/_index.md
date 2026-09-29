---
title: PdfSaveOptions constructor
linktitle: PdfSaveOptions constructor
articleTitle: PdfSaveOptions constructor
second_title: Aspose.Words for Python
description: "PdfSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../../aspose.words/saveformat/#PDF) format."
type: docs
weight: 10
url: /es/python-net/aspose.words.saving/pdfsaveoptions/__init__/
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
# Configure nuestras fuentes de origen para asegurarnos de que tenemos acceso a ambas fuentes en este documento.
original_fonts_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=[original_fonts_sources[0], folder_font_source])
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in font_sources[1].get_available_fonts()]))
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Dado que nuestro documento contiene una fuente personalizada, incrustarla en el documento de salida puede ser deseable.
# Establezca la propiedad "EmbedFullFonts" a "true" para incrustar cada glifo de todas las fuentes incrustadas en el PDF de salida.
# El tamaño del documento puede volverse muy grande, pero tendremos pleno uso de todas las fuentes si editamos el PDF.
# Establezca la propiedad "EmbedFullFonts" en "false" para aplicar subconfiguración a las fuentes, guardando solo los glifos
# que el documento está usando. El archivo será considerablemente más pequeño,
# pero es posible que necesitemos acceso a cualquier fuente personalizada si editamos el documento.
options.embed_full_fonts = embed_full_fonts
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedFullFonts.pdf', save_options=options)
# Restaurar las fuentes originales.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_fonts_sources)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

