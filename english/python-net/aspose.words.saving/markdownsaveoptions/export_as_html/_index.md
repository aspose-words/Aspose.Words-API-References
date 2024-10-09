---
title: MarkdownSaveOptions.export_as_html property
linktitle: export_as_html property
articleTitle: export_as_html property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.export_as_html property. Allows to specify the elements to be exported to Markdown as raw HTML"
type: docs
weight: 20
url: /python-net/aspose.words.saving/markdownsaveoptions/export_as_html/
---

## MarkdownSaveOptions.export_as_html property

Allows to specify the elements to be exported to Markdown as raw HTML.
Default value is [MarkdownExportAsHtml.NONE](../../markdownexportashtml/#NONE).



```python
@property
def export_as_html(self) -> aspose.words.saving.MarkdownExportAsHtml:
    ...

@export_as_html.setter
def export_as_html(self, value: aspose.words.saving.MarkdownExportAsHtml):
    ...

```

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

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

