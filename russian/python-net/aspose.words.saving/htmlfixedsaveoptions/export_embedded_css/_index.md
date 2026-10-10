---
title: HtmlFixedSaveOptions.export_embedded_css property
linktitle: export_embedded_css property
articleTitle: export_embedded_css property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_css property. Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document."
type: docs
weight: 40
url: /ru/python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_css/
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
# При экспорте документа в html, Aspose.Words также создаст таблицу стилей CSS для форматирования документа.
# Установка флага "ExportEmbeddedCss" в "true" сохраняет таблицу стилей CSS в файл .css,
# и связывает файл с html‑документом с помощью элемента <link>.
# Установка флага в "false" встроит таблицу стилей CSS в документ Html,
# что создаст только один файл вместо двух.
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

