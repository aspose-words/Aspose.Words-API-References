---
title: HtmlElementSizeOutputMode enumeration
linktitle: HtmlElementSizeOutputMode enumeration
articleTitle: HtmlElementSizeOutputMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HtmlElementSizeOutputMode enumeration. Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB."
type: docs
weight: 230
url: /tr/python-net/aspose.words.saving/htmlelementsizeoutputmode/
---

## HtmlElementSizeOutputMode enumeration

Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB.


### Members

| Name | Description |
| --- | --- |
| ALL | All element sizes, both in absolute and relative units, specified in the document are exported. |
| RELATIVE_ONLY | Element sizes are exported only if they are specified in relative units in the document.  Fixed sizes are not exported in this mode. Visual agents will calculate missing sizes to make  document layout more natural. |
| NONE | Element sizes are not exported. Visual agents will build layout automatically according to relationship between elements. |

### Examples

Shows how to preserve negative indents in the output .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Negatif girintiyle bir tablo ekleyin, bu tabloyu sol sayfa sınırının ötesine sola itecektir.
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1')
builder.insert_cell()
builder.write('Row 1, Cell 2')
builder.end_table()
table.left_indent = -36
table.preferred_width = aw.tables.PreferredWidth.from_points(144)
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
# Pozitif girintiyle bir tablo ekleyin, bu tabloyu sağa itecektir.
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1')
builder.insert_cell()
builder.write('Row 1, Cell 2')
builder.end_table()
table.left_indent = 36
table.preferred_width = aw.tables.PreferredWidth.from_points(144)
# Bir belgeyi HTML olarak kaydettiğimizde, Aspose.Words yalnızca negatif girintileri korur
# örneğin, "AllowNegativeIndent" bayrağını "true" olarak ayarladığımızda ilk tabloya uyguladığımız gibi
# "true" olarak geçireceğimiz bir SaveOptions nesnesinde
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.allow_negative_indent = allow_negative_indent
options.table_width_output_mode = aw.saving.HtmlElementSizeOutputMode.RELATIVE_ONLY
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.NegativeIndent.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.NegativeIndent.html')
if allow_negative_indent:
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
else:
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.table_width_output_mode](../htmlsaveoptions/table_width_output_mode/)

