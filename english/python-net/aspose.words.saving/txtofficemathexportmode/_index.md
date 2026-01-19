---
title: TxtOfficeMathExportMode enumeration
linktitle: TxtOfficeMathExportMode enumeration
articleTitle: TxtOfficeMathExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TxtOfficeMathExportMode enumeration. Specifies how Aspose.Words exports OfficeMath to [SaveFormat.TEXT](../../aspose.words/saveformat/#TEXT)."
type: docs
weight: 890
url: /python-net/aspose.words.saving/txtofficemathexportmode/
---

## TxtOfficeMathExportMode enumeration

Specifies how Aspose.Words exports OfficeMath to [SaveFormat.TEXT](../../aspose.words/saveformat/#TEXT).



### Members

| Name | Description |
| --- | --- |
| TEXT | Export OfficeMath as plain text. |
| LATEX | Export OfficeMath as LaTeX. |

### Examples

Shows how to export OfficeMath object as Latex in TXT.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
save_options = aw.saving.TxtSaveOptions()
save_options.office_math_export_mode = aw.saving.TxtOfficeMathExportMode.LATEX
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.ExportOfficeMathAsLatexToText.txt', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

