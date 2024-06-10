---
title: HtmlSaveOptions.table_width_output_mode property
linktitle: table_width_output_mode property
articleTitle: table_width_output_mode property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.table_width_output_mode property. Controls how table, row and cell widths are exported to HTML, MHTML or EPUB"
type: docs
weight: 460
url: /python-net/aspose.words.saving/htmlsaveoptions/table_width_output_mode/
---

## HtmlSaveOptions.table_width_output_mode property

Controls how table, row and cell widths are exported to HTML, MHTML or EPUB.
Default value is [HtmlElementSizeOutputMode.ALL](../../htmlelementsizeoutputmode/#ALL).



```python
@property
def table_width_output_mode(self) -> aspose.words.saving.HtmlElementSizeOutputMode:
    ...

@table_width_output_mode.setter
def table_width_output_mode(self, value: aspose.words.saving.HtmlElementSizeOutputMode):
    ...

```

### Remarks

In the HTML format, table, row and cell elements 
(**\<table\>**, **\<tr\>**, **\<th\>**, **\<td\>**)
can have their widths specified either in relative (percentage) or in absolute units.
In a document in Aspose.Words, tables, rows and cells can have their widths specified 
using either relative or absolute units too.

When you convert a document to HTML using Aspose.Words, you might want to control how
table, row and cell widths are exported to affect how the resulting document is displayed 
in the visual agent (e.g. a browser or viewer).

Use this property as a filter to specify what table widths values are exported into the destination document.
For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device,
then you probably want to avoid exporting absolute width values. To do this you need to specify 
the output mode [HtmlElementSizeOutputMode.RELATIVE_ONLY](../../htmlelementsizeoutputmode/#RELATIVE_ONLY) or [HtmlElementSizeOutputMode.NONE](../../htmlelementsizeoutputmode/#NONE)
so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can.




### Examples

Shows how to preserve negative indents in the output .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a table with a negative indent, which will push it to the left past the left page boundary.
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1')
builder.insert_cell()
builder.write('Row 1, Cell 2')
builder.end_table()
table.left_indent = -36
table.preferred_width = aw.tables.PreferredWidth.from_points(144)
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
# Insert a table with a positive indent, which will push the table to the right.
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1')
builder.insert_cell()
builder.write('Row 1, Cell 2')
builder.end_table()
table.left_indent = 36
table.preferred_width = aw.tables.PreferredWidth.from_points(144)
# When we save a document to HTML, Aspose.Words will only preserve negative indents
# such as the one we have applied to the first table if we set the "allow_negative_indent" flag
# in a SaveOptions object that we will pass to "True".
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.allow_negative_indent = allow_negative_indent
options.table_width_output_mode = aw.saving.HtmlElementSizeOutputMode.RELATIVE_ONLY
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.negative_indent.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.negative_indent.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if allow_negative_indent:
    self.assertIn('<table cellspacing="0" cellpadding="0" style="margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">', out_doc_contents)
    self.assertIn('<table cellspacing="0" cellpadding="0" style="margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">', out_doc_contents)
else:
    self.assertIn('<table cellspacing="0" cellpadding="0" style="border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">', out_doc_contents)
    self.assertIn('<table cellspacing="0" cellpadding="0" style="margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">', out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

