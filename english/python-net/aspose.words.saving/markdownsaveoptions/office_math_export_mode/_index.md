---
title: MarkdownSaveOptions.office_math_export_mode property
linktitle: office_math_export_mode property
articleTitle: office_math_export_mode property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.office_math_export_mode property. Specifies how OfficeMath will be written to the output file"
type: docs
weight: 120
url: /python-net/aspose.words.saving/markdownsaveoptions/office_math_export_mode/
---

## MarkdownSaveOptions.office_math_export_mode property

Specifies how OfficeMath will be written to the output file.
Default value is [MarkdownOfficeMathExportMode.TEXT](../../markdownofficemathexportmode/#TEXT).



```python
@property
def office_math_export_mode(self) -> aspose.words.saving.MarkdownOfficeMathExportMode:
    ...

@office_math_export_mode.setter
def office_math_export_mode(self, value: aspose.words.saving.MarkdownOfficeMathExportMode):
    ...

```

### Examples

Shows how OfficeMath will be written to the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
save_options = aw.saving.MarkdownSaveOptions()
save_options.office_math_export_mode = aw.saving.MarkdownOfficeMathExportMode.IMAGE
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.OfficeMathExportMode.md', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

