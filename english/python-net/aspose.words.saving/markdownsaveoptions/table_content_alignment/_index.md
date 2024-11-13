---
title: MarkdownSaveOptions.table_content_alignment property
linktitle: table_content_alignment property
articleTitle: table_content_alignment property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.table_content_alignment property. Gets or sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format"
type: docs
weight: 110
url: /python-net/aspose.words.saving/markdownsaveoptions/table_content_alignment/
---

## MarkdownSaveOptions.table_content_alignment property

Gets or sets a value that specifies how to align contents in tables
when exporting into the [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format.
The default value is [TableContentAlignment.AUTO](../../tablecontentalignment/#AUTO).



```python
@property
def table_content_alignment(self) -> aspose.words.saving.TableContentAlignment:
    ...

@table_content_alignment.setter
def table_content_alignment(self, value: aspose.words.saving.TableContentAlignment):
    ...

```

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

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

