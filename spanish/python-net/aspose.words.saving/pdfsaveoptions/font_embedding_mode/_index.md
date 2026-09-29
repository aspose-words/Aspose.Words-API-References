---
title: PdfSaveOptions.font_embedding_mode property
linktitle: font_embedding_mode property
articleTitle: font_embedding_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.font_embedding_mode property. Specifies the font embedding mode."
type: docs
weight: 180
url: /es/python-net/aspose.words.saving/pdfsaveoptions/font_embedding_mode/
---

## PdfSaveOptions.font_embedding_mode property

Specifies the font embedding mode.


```python
@property
def font_embedding_mode(self) -> aspose.words.saving.PdfFontEmbeddingMode:
    ...

@font_embedding_mode.setter
def font_embedding_mode(self, value: aspose.words.saving.PdfFontEmbeddingMode):
    ...

```

### Remarks

The default value is [PdfFontEmbeddingMode.EMBED_ALL](../../pdffontembeddingmode/#EMBED_ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains
non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.
[PdfFontEmbeddingMode.EMBED_ALL](../../pdffontembeddingmode/#EMBED_ALL) value will be used automatically when saving to
PDF/A and PDF/UA.




### Examples

Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# "Arial" es una fuente estándar, y "Courier New" es una fuente no estándar.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "EmbedFullFonts" a "true" para incrustar cada glifo de todas las fuentes incrustadas en el PDF de salida.
options.embed_full_fonts = True
# Establezca la propiedad "FontEmbeddingMode" a "EmbedAll" para incrustar todas las fuentes en el PDF de salida.
# Establezca la propiedad "FontEmbeddingMode" a "EmbedNonstandard" para permitir únicamente la incrustación de fuentes no estándar en el PDF de salida.
# Establezca la propiedad "FontEmbeddingMode" a "EmbedNone" para no incrustar ninguna fuente en el PDF de salida.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

