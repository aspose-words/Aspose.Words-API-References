---
title: HtmlFixedSaveOptions.export_embedded_css property
linktitle: export_embedded_css property
articleTitle: export_embedded_css property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_css property. Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document."
type: docs
weight: 40
url: /de/python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_css/
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
# Wenn Sie ein Dokument nach html exportieren, erstellt Aspose.Words außerdem ein CSS-Stylesheet, um das Dokument zu formatieren.
# Das Setzen des Flags "ExportEmbeddedCss" auf "true" speichert das CSS-Stylesheet in einer .css-Datei,
# und verlinkt die Datei aus dem html-Dokument mittels eines <link>-Elements.
# Das Setzen des Flags auf "false" bettet das CSS-Stylesheet in das Html-Dokument ein,
# die nur eine Datei anstelle von zwei erstellt.
html_fixed_save_options = aw_saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_css = export_embedded_css
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedCss.html', save_options=html_fixed_save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedCss.html')
if export_embedded_css:
    assert re.search('<style type="text/css">', out_doc_contents) is not None
    assert not system_helper.io.File.exist(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css')
else:
    assert re.search('<link rel="stylesheet" type="text/css" href="HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css" media="all" />', out_doc_contents) is not None
    assert system_helper.io.File.exist(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css')
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

