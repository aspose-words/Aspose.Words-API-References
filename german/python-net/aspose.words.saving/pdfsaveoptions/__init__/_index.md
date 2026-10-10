---
title: PdfSaveOptions constructor
linktitle: PdfSaveOptions constructor
articleTitle: PdfSaveOptions constructor
second_title: Aspose.Words for Python
description: "PdfSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../../aspose.words/saveformat/#PDF) format."
type: docs
weight: 10
url: /de/python-net/aspose.words.saving/pdfsaveoptions/__init__/
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
# Konfigurieren Sie unsere Schriftquellen, um sicherzustellen, dass wir Zugriff auf beide Schriftarten in diesem Dokument haben.
original_fonts_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=True)
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=[original_fonts_sources[0], folder_font_source])
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertTrue(any([f.full_font_name == 'Arvo' for f in font_sources[1].get_available_fonts()]))
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Da unser Dokument eine benutzerdefinierte Schriftart enthält, kann das Einbetten in das Ausgabedokument wünschenswert sein.
# Setzen Sie die Eigenschaft "EmbedFullFonts" auf "true", um jedes Glyph jedes eingebetteten Schriftsatzes im ausgegebenen PDF zu integrieren.
# Die Größe des Dokuments kann sehr groß werden, aber wir haben die volle Nutzung aller Schriftarten, wenn wir das PDF bearbeiten.
# Setzen Sie die Eigenschaft "EmbedFullFonts" auf "false", um Font-Subsetting anzuwenden und nur die Glyphen zu speichern
# die das Dokument verwendet. Die Datei wird deutlich kleiner sein,
# aber wir benötigen möglicherweise Zugriff auf alle benutzerdefinierten Schriftarten, wenn wir das Dokument bearbeiten.
options.embed_full_fonts = embed_full_fonts
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedFullFonts.pdf', save_options=options)
# Stellen Sie die ursprünglichen Schriftquellen wieder her.
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_fonts_sources)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

