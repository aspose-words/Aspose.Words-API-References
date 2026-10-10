---
title: HtmlSaveOptions.export_page_margins property
linktitle: export_page_margins property
articleTitle: export_page_margins property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_page_margins property. Specifies whether page margins is exported to HTML, MHTML or EPUB"
type: docs
weight: 210
url: /de/python-net/aspose.words.saving/htmlsaveoptions/export_page_margins/
---

## HtmlSaveOptions.export_page_margins property

Specifies whether page margins is exported to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_page_margins(self) -> bool:
    ...

@export_page_margins.setter
def export_page_margins(self, value: bool):
    ...

```

### Remarks

Aspose.Words does not show area of page margins by default.
If any elements are completely or partially clipped by the document edge the displayed area can be extended with
this option.


### Examples

Shows how to show out-of-bounds objects in output HTML documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Verwenden Sie einen Builder, um eine Form ohne Textumbruch einzufügen.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=200, height=200)
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.wrap_type = aw.drawing.WrapType.NONE
# Negative Positionswerte der Form können die Form außerhalb der Seitenränder platzieren.
# Wenn wir dies nach HTML exportieren, wird die Form abgeschnitten angezeigt.
shape.left = -150
# Beim Speichern des Dokuments als HTML können wir ein SaveOptions‑Objekt übergeben
# um zu entscheiden, ob die Seite angepasst werden soll, um Objekte außerhalb der Grenzen vollständig anzuzeigen.
# Wenn wir das Flag "ExportPageMargins" auf "true" setzen, wird die Form im ausgegebenen HTML vollständig sichtbar sein.
# Wenn wir das Flag "ExportPageMargins" auf "false" setzen,
# wird unser Dokument die Form abgeschnitten anzeigen, wie wir sie in Microsoft Word sehen würden.
options = aw.saving.HtmlSaveOptions()
options.export_page_margins = export_page_margins
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageMargins.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageMargins.html')
if export_page_margins:
    self.assertTrue('<style type="text/css">div.Section_1 { margin:70.85pt }</style>' in out_doc_contents)
    self.assertTrue('<div class="Section_1"><p style="margin-top:0pt; margin-left:150pt; margin-bottom:0pt">' in out_doc_contents)
else:
    self.assertFalse('style type="text/css">' in out_doc_contents)
    self.assertTrue('<div><p style="margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt">' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

