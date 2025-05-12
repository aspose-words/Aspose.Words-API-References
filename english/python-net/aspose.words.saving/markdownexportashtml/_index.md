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

### See Also

* module [aspose.words.saving](../)

