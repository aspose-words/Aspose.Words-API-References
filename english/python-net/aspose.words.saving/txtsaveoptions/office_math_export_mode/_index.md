---
title: TxtSaveOptions.office_math_export_mode property
linktitle: office_math_export_mode property
articleTitle: office_math_export_mode property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.office_math_export_mode property. Specifies how OfficeMath will be written to the output file"
type: docs
weight: 50
url: /python-net/aspose.words.saving/txtsaveoptions/office_math_export_mode/
---

## TxtSaveOptions.office_math_export_mode property

Specifies how OfficeMath will be written to the output file.
Default value is [TxtOfficeMathExportMode.TEXT](../../txtofficemathexportmode/#TEXT).



```python
@property
def office_math_export_mode(self) -> aspose.words.saving.TxtOfficeMathExportMode:
    ...

@office_math_export_mode.setter
def office_math_export_mode(self, value: aspose.words.saving.TxtOfficeMathExportMode):
    ...

```

### Examples

Shows how to export OfficeMath object as Latex in TXT.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
save_options = aw.saving.TxtSaveOptions()
save_options.office_math_export_mode = aw.saving.TxtOfficeMathExportMode.LATEX
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.ExportOfficeMathAsLatexToText.txt', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

