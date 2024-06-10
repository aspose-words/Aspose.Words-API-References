---
title: HtmlFixedSaveOptions.export_embedded_css property
linktitle: export_embedded_css property
articleTitle: export_embedded_css property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_css property. Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document."
type: docs
weight: 40
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_css/
---

## HtmlFixedSaveOptions.export_embedded_css property

Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.


```python
@property
def export_embedded_css(self) -> bool:
    ...

@export_embedded_css.setter
def export_embedded_css(self, value: bool):
    ...

```

### Examples

Shows how to determine where to store CSS stylesheets when exporting a document to Html.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
# When we export a document to html, Aspose.Words will also create a CSS stylesheet to format the document with.
# Setting the "html_fixed_save_options" flag to "True" save the CSS stylesheet to a .css file,
# and link to the file from the html document using a <link> element.
# Setting the flag to "False" will embed the CSS stylesheet within the Html document,
# which will create only one file instead of two.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_css = export_embedded_css
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_css.html', html_fixed_save_options)
with open(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_css.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if export_embedded_css:
    self.assertIn('<style type="text/css">', out_doc_contents)
    self.assertFalse(os.path.exists(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_css/styles.css'))
else:
    self.assertIn('<link rel="stylesheet" type="text/css" href="HtmlFixedSaveOptions.export_embedded_css/styles.css" media="all" />', out_doc_contents)
    self.assertTrue(os.path.exists(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.export_embedded_css/styles.css'))
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

