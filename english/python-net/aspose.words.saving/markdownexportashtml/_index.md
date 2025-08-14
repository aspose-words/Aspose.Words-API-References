---
title: MarkdownExportAsHtml enumeration
linktitle: MarkdownExportAsHtml enumeration
articleTitle: MarkdownExportAsHtml enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MarkdownExportAsHtml enumeration. Allows to specify the elements to be exported to Markdown as raw HTML."
type: docs
weight: 430
url: /python-net/aspose.words.saving/markdownexportashtml/
---

## MarkdownExportAsHtml enumeration

Allows to specify the elements to be exported to Markdown as raw HTML.


### Members

| Name | Description |
| --- | --- |
| NONE | Export all elements using Markdown syntax without any raw HTML. |
| TABLES | Export tables as raw HTML. |
| NON_COMPATIBLE_TABLES | Export tables that cannot be correctly represented in pure Markdown as raw HTML. |

### Examples

Shows how to export a table to Markdown as raw HTML.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Sample table:')
# Create table.
builder.insert_cell()
builder.paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
builder.write('Cell1')
builder.insert_cell()
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write('Cell2')
save_options = aw.saving.MarkdownSaveOptions()
save_options.export_as_html = aw.saving.MarkdownExportAsHtml.TABLES
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ExportTableAsHtml.md', save_options=save_options)
```

Shows how to export tables that cannot be correctly represented in pure Markdown as raw HTML.

```python
output_path = ARTIFACTS_DIR + 'MarkdownSaveOptions.NonCompatibleTables.md'
doc = aw.Document(file_name=MY_DIR + 'Non compatible table.docx')
# With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
# or nested tables to raw HTML and leave simple tables in Markdown format.
save_options = aw.saving.MarkdownSaveOptions()
save_options.export_as_html = aw.saving.MarkdownExportAsHtml.NON_COMPATIBLE_TABLES
doc.save(file_name=output_path, save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

