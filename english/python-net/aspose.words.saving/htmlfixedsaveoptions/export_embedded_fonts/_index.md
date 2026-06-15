---
title: HtmlFixedSaveOptions.export_embedded_fonts property
linktitle: export_embedded_fonts property
articleTitle: export_embedded_fonts property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_fonts property. Specifies whether fonts should be embedded into Html document in Base64 format"
type: docs
weight: 50
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_fonts/
---

## HtmlFixedSaveOptions.export_embedded_fonts property

Specifies whether fonts should be embedded into Html document in Base64 format.
Note setting this flag can significantly increase size of output Html file.


```python
@property
def export_embedded_fonts(self) -> bool:
    ...

@export_embedded_fonts.setter
def export_embedded_fonts(self, value: bool):
    ...

```

### Examples

Shows how to determine where to store embedded fonts when exporting a document to Html.

```python
doc = aw.Document(MY_DIR + 'Embedded font.docx')
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_fonts = export_embedded_fonts
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedFonts.html', save_options=html_fixed_save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css')
if export_embedded_fonts:
    assert re.search("@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }", out_doc_contents)
    self.assertEqual(0, len(list(filter(lambda f: f.endswith('.woff'), system_helper.io.Directory.get_files(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedFonts')))))
else:
    assert re.search("@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }", out_doc_contents)
    self.assertEqual(2, len(list(filter(lambda f: f.endswith('.woff'), system_helper.io.Directory.get_files(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedFonts')))))
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

