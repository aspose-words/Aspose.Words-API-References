---
title: HtmlSaveOptions.resolve_font_names property
linktitle: resolve_font_names property
articleTitle: resolve_font_names property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.resolve_font_names property. Specifies whether font family names used in the document are resolved and substituted according to [Document.font_settings](../../../aspose.words/document/font_settings/) when being written into HTML-based formats."
type: docs
weight: 430
url: /de/python-net/aspose.words.saving/htmlsaveoptions/resolve_font_names/
---

## HtmlSaveOptions.resolve_font_names property

Specifies whether font family names used in the document are resolved and substituted according to
[Document.font_settings](../../../aspose.words/document/font_settings/) when being written into HTML-based formats.



```python
@property
def resolve_font_names(self) -> bool:
    ...

@resolve_font_names.setter
def resolve_font_names(self, value: bool):
    ...

```

### Remarks

By default, this option is set to ``False`` and font family names are written to HTML as specified
in source documents. That is, [Document.font_settings](../../../aspose.words/document/font_settings/) are ignored and no resolution or substitution
of font family names is performed.

If this option is set to ``True``, Aspose.Words uses [Document.font_settings](../../../aspose.words/document/font_settings/) to resolve
each font family name specified in a source document into the name of an available font family, performing
font substitution as required.




### Examples

Shows how to resolve all font names before writing them to HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Dieses Dokument enthält Text, der eine Schriftart nennt, die wir nicht besitzen.
self.assertIsNotNone(doc.font_infos.get_by_name('28 Days Later'))
# Wenn wir keine Möglichkeit haben, diese Schriftart zu erhalten, und wir den gesamten Text anzeigen können wollen
# in diesem Dokument in einem Ausgabe‑HTML, können wir sie durch eine andere Schriftart ersetzen.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.default_font_substitution.enabled = True
doc.font_settings = font_settings
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
# Standardmäßig ist diese Option auf 'False' gesetzt und Aspose.Words schreibt Schriftartnamen wie im Quell‑Dokument angegeben.
save_options.resolve_font_names = resolve_font_names
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ResolveFontNames.html', save_options=save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ResolveFontNames.html')
expected = '<span style="font-family:Arial">' if resolve_font_names else '<span style="font-family:\'28 Days Later\'">'
self.assertTrue(re.search(expected, out_doc_contents) is not None)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

