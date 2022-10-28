---
title: resolve_font_names property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether font family names used in the document are resolved and substituted according to [Document.font_settings](../../../aspose.words/document/font_settings/) when being written into HTML-based formats."
type: docs
weight: 410
url: /python-net/aspose.words.saving/htmlsaveoptions/resolve_font_names/
---

## HtmlSaveOptions.resolve_font_names property

Specifies whether font family names used in the document are resolved and substituted according to
[Document.font_settings](../../../aspose.words/document/font_settings/) when being written into HTML-based formats.


By default, this option is set to ``False`` and font family names are written to HTML as specified
in source documents. That is, [Document.font_settings](../../../aspose.words/document/font_settings/) are ignored and no resolution or substitution
of font family names is performed.

If this option is set to ``True``, Aspose.Words uses [Document.font_settings](../../../aspose.words/document/font_settings/) to resolve
each font family name specified in a source document into the name of an available font family, performing
font substitution as required.




### Examples

Shows how to resolve all font names before writing them to HTML.

```python
doc = aw.Document(MY_DIR + "Missing font.docx")

# This document contains text that names a font that we do not have.
self.assertIsNotNone(doc.font_infos.get_by_name("28 Days Later"))

# If we have no way of getting this font, and we want to be able to display all the text
# in this document in an output HTML, we can substitute it with another font.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = "Arial"
font_settings.substitution_settings.default_font_substitution.enabled = True

doc.font_settings = font_settings

save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)

# By default, this option is set to 'False' and Aspose.Words writes font names as specified in the source document
save_options.resolve_font_names = resolve_font_names

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.resolve_font_names.html", save_options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.resolve_font_names.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if resolve_font_names:
    self.assertIn("<span style=\"font-family:Arial\">", out_doc_contents)
else:
    self.assertIn("<span style=\"font-family:'28 Days Later'\">", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

