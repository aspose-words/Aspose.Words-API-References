---
title: TableContentAlignment enumeration
linktitle: TableContentAlignment enumeration
articleTitle: TableContentAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TableContentAlignment enumeration. Allows to specify the alignment of the content of the table to be used when exporting into Markdown format."
type: docs
weight: 810
url: /python-net/aspose.words.saving/tablecontentalignment/
---

## TableContentAlignment enumeration

Allows to specify the alignment of the content of the table to be used when exporting into Markdown format.


### Members

| Name | Description |
| --- | --- |
| AUTO | The alignment will be taken from the first paragraph in corresponding table column. |
| LEFT | The content of tables will be aligned to the Left. |
| CENTER | The content of tables will be aligned to the Center. |
| RIGHT | The content of tables will be aligned to the Right. |

### Examples

Shows how to align contents in tables.

```python
builder = aw.DocumentBuilder()
builder.insert_cell()
builder.paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
builder.write('Cell1')
builder.insert_cell()
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write('Cell2')
save_options = aw.saving.MarkdownSaveOptions()
save_options.table_content_alignment = table_content_alignment
builder.document.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md', save_options=save_options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md')
table = doc.first_section.body.tables[0]
switch_condition = table_content_alignment
if switch_condition == aw.saving.TableContentAlignment.AUTO:
    self.assertEqual(aw.ParagraphAlignment.RIGHT, table.first_row.cells[0].first_paragraph.paragraph_format.alignment)
    self.assertEqual(aw.ParagraphAlignment.CENTER, table.first_row.cells[1].first_paragraph.paragraph_format.alignment)
elif switch_condition == aw.saving.TableContentAlignment.LEFT:
    self.assertEqual(aw.ParagraphAlignment.LEFT, table.first_row.cells[0].first_paragraph.paragraph_format.alignment)
    self.assertEqual(aw.ParagraphAlignment.LEFT, table.first_row.cells[1].first_paragraph.paragraph_format.alignment)
elif switch_condition == aw.saving.TableContentAlignment.CENTER:
    self.assertEqual(aw.ParagraphAlignment.CENTER, table.first_row.cells[0].first_paragraph.paragraph_format.alignment)
    self.assertEqual(aw.ParagraphAlignment.CENTER, table.first_row.cells[1].first_paragraph.paragraph_format.alignment)
elif switch_condition == aw.saving.TableContentAlignment.RIGHT:
    self.assertEqual(aw.ParagraphAlignment.RIGHT, table.first_row.cells[0].first_paragraph.paragraph_format.alignment)
    self.assertEqual(aw.ParagraphAlignment.RIGHT, table.first_row.cells[1].first_paragraph.paragraph_format.alignment)
```

### See Also

* module [aspose.words.saving](../)

