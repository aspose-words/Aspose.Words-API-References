﻿---
title: HtmlSaveOptions.allow_negative_indent property
linktitle: allow_negative_indent property
articleTitle: allow_negative_indent property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.allow_negative_indent property. Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB"
type: docs
weight: 20
url: /python-net/aspose.words.saving/htmlsaveoptions/allow_negative_indent/
---

## HtmlSaveOptions.allow_negative_indent property

Specifies whether negative left and right indents of paragraphs are normalized
when saving to HTML, MHTML or EPUB. Default value is ``False``.



```python
@property
def allow_negative_indent(self) -> bool:
    ...

@allow_negative_indent.setter
def allow_negative_indent(self, value: bool):
    ...

```

### Remarks

When negative indent is not allowed, it is exported as zero margin to HTML.
When negative indent is allowed, a paragraph might appear partially outside of the
browser window.




### Examples

Shows how to preserve negative indents in the output .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
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
# such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
# in a SaveOptions object that we will pass to "true".
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.allow_negative_indent = allow_negative_indent
options.table_width_output_mode = aw.saving.HtmlElementSizeOutputMode.RELATIVE_ONLY
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.NegativeIndent.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.NegativeIndent.html')
if allow_negative_indent:
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
else:
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

