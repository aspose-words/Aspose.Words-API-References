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
# When we export a document with embedded fonts to .html,
# Aspose.Words can place the fonts in two possible locations.
# Setting the "export_embedded_fonts" flag to "True" will store the raw data for embedded fonts within the CSS stylesheet,
# in the "url" property of the "@font-face" rule. This may create a huge CSS stylesheet file
# and reduce the number of external files that this HTML conversion will create.
# Setting this flag to "False" will create a file for each font.
# The CSS stylesheet will link to each font file using the "url" property of the "@font-face" rule.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_fonts = export_embedded_fonts
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_fonts.html', html_fixed_save_options)
with open(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_fonts/styles.css', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if export_embedded_fonts:
    self.assertRegex(out_doc_contents, "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")
    self.assertEqual(0, len(glob.glob(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_fonts/*.woff')))
else:
    self.assertRegex(out_doc_contents, "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")
    self.assertEqual(2, len(glob.glob(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_fonts/*.woff')))
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

