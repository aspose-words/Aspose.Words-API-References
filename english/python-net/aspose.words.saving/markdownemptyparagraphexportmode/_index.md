---
title: MarkdownEmptyParagraphExportMode enumeration
linktitle: MarkdownEmptyParagraphExportMode enumeration
articleTitle: MarkdownEmptyParagraphExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MarkdownEmptyParagraphExportMode enumeration. Specifies how Aspose.Words exports empty paragraphs to Markdown."
type: docs
weight: 430
url: /python-net/aspose.words.saving/markdownemptyparagraphexportmode/
---

## MarkdownEmptyParagraphExportMode enumeration

Specifies how Aspose.Words exports empty paragraphs to Markdown.


### Members

| Name | Description |
| --- | --- |
| EMPTY_LINE | Export as empty lines. |
| MARKDOWN_HARD_LINE_BREAK | Export as Markdown HardLineBreak character '\\'. |
| NONE | Don't export empty paragraphs. |

### Examples

Shows how to export empty paragraphs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('First')
builder.writeln('\r\n\r\n\r\n')
builder.writeln('Last')
save_options = aw.saving.MarkdownSaveOptions()
save_options.empty_paragraph_export_mode = export_mode
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.EmptyParagraphExportMode.md', save_options=save_options)
result = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'MarkdownSaveOptions.EmptyParagraphExportMode.md')
switch_condition = export_mode
if switch_condition == aw.saving.MarkdownEmptyParagraphExportMode.NONE:
    self.assertEqual('First\r\n\r\nLast\r\n', result)
elif switch_condition == aw.saving.MarkdownEmptyParagraphExportMode.EMPTY_LINE:
    self.assertEqual('First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n', result)
elif switch_condition == aw.saving.MarkdownEmptyParagraphExportMode.MARKDOWN_HARD_LINE_BREAK:
    self.assertEqual('First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n', result)
```

### See Also

* module [aspose.words.saving](../)

