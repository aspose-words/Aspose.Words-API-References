---
title: PdfSaveOptions.font_embedding_mode property
linktitle: font_embedding_mode property
articleTitle: font_embedding_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.font_embedding_mode property. Specifies the font embedding mode."
type: docs
weight: 180
url: /de/python-net/aspose.words.saving/pdfsaveoptions/font_embedding_mode/
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
# "Arial" ist eine Standardschriftart, und "Courier New" ist eine nicht‑standardmäßige Schriftart.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "EmbedFullFonts" auf "true", um jedes Glyph jedes eingebetteten Schriftsatzes im ausgegebenen PDF zu integrieren.
options.embed_full_fonts = True
# Setzen Sie die Eigenschaft "FontEmbeddingMode" auf "EmbedAll", um alle Schriften im ausgegebenen PDF einzubetten.
# Setzen Sie die Eigenschaft "FontEmbeddingMode" auf "EmbedNonstandard", um das Einbetten nur nicht‑standardmäßiger Schriften im ausgegebenen PDF zu erlauben.
# Setzen Sie die Eigenschaft "FontEmbeddingMode" auf "EmbedNone", um keine Schriften im ausgegebenen PDF einzubetten.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

