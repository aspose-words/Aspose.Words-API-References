---
title: MarkdownOfficeMathExportMode enumeration
linktitle: MarkdownOfficeMathExportMode enumeration
articleTitle: MarkdownOfficeMathExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MarkdownOfficeMathExportMode enumeration. Specifies how Aspose.Words exports OfficeMath to Markdown."
type: docs
weight: 460
url: /python-net/aspose.words.saving/markdownofficemathexportmode/
---

## MarkdownOfficeMathExportMode enumeration

Specifies how Aspose.Words exports OfficeMath to Markdown.


### Members

| Name | Description |
| --- | --- |
| TEXT | Export OfficeMath as plain text. |
| IMAGE | Export OfficeMath as image. |
| MATH_ML | Export OfficeMath as MathML. |
| LATEX | Export OfficeMath as LaTeX. |
| MARK_IT_DOWN | Export OfficeMath as LaTeX that is compatible with MarkItDown. |

### Examples

Shows how OfficeMath will be written to the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
save_options = aw.saving.MarkdownSaveOptions()
save_options.office_math_export_mode = aw.saving.MarkdownOfficeMathExportMode.IMAGE
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.OfficeMathExportMode.md', save_options=save_options)
```

Shows how to export OfficeMath object as Latex.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
save_options = aw.saving.MarkdownSaveOptions()
save_options.office_math_export_mode = aw.saving.MarkdownOfficeMathExportMode.LATEX
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ExportOfficeMathAsLatex.md', save_options=save_options)
```

Shows how to export OfficeMath object as MarkItDown.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
save_options = aw.saving.MarkdownSaveOptions()
save_options.office_math_export_mode = aw.saving.MarkdownOfficeMathExportMode.MARK_IT_DOWN
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

