---
title: SaveOptions.allow_embedding_post_script_fonts property
linktitle: allow_embedding_post_script_fonts property
articleTitle: allow_embedding_post_script_fonts property
second_title: Aspose.Words for Python
description: "SaveOptions.allow_embedding_post_script_fonts property. Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved"
type: docs
weight: 10
url: /python-net/aspose.words.saving/saveoptions/allow_embedding_post_script_fonts/
---

## SaveOptions.allow_embedding_post_script_fonts property

Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines
when embedding TrueType fonts in a document upon it is saved.
The default value is ``False``.


Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.embed_true_type_fonts](../../../aspose.words.fonts/fontinfocollection/embed_true_type_fonts/) of the
[DocumentBase.font_infos](../../../aspose.words/documentbase/font_infos/) property is set to ``True``.




### Examples

Shows how to save the document with PostScript font.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "PostScriptFont"
builder.writeln("Some text with PostScript font.")

# Load the font with PostScript to use in the document.
with open(FONTS_DIR + "AllegroOpen.otf", "rb") as file:
    otf = aw.fonts.MemoryFontSource(file.read())

doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.set_fonts_sources([otf])

# Embed TrueType fonts.
doc.font_infos.embed_true_type_fonts = True

# Allow embedding PostScript fonts while embedding TrueType fonts.
# Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
save_options = aw.saving.SaveOptions.create_save_options(aw.SaveFormat.DOCX)
save_options.allow_embedding_post_script_fonts = True

doc.save(ARTIFACTS_DIR + "Document.allow_embedding_post_script_fonts.docx", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

