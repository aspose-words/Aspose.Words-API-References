---
title: XlsxSaveOptions.section_mode property
linktitle: section_mode property
articleTitle: section_mode property
second_title: Aspose.Words for Python
description: "XlsxSaveOptions.section_mode property. Gets or sets the way how sections are handled when saving to the output XLSX document"
type: docs
weight: 40
url: /python-net/aspose.words.saving/xlsxsaveoptions/section_mode/
---

## XlsxSaveOptions.section_mode property

Gets or sets the way how sections are handled when saving to the output XLSX document.
The default value is [XlsxSectionMode.MULTIPLE_WORKSHEETS](../../xlsxsectionmode/#MULTIPLE_WORKSHEETS).



```python
@property
def section_mode(self) -> aspose.words.saving.XlsxSectionMode:
    ...

@section_mode.setter
def section_mode(self, value: aspose.words.saving.XlsxSectionMode):
    ...

```

### Examples

Shows how to save document as a separate worksheets.

```python
doc = Document(MY_DIR + "Big document.docx")

# Each section of a document will be created as a separate worksheet.
# Use 'SingleWorksheet' to display all document on one worksheet.

xlsx_save_options = XlsxSaveOptions()
xlsx_save_options.section_mode = XlsxSectionMode.MULTIPLE_WORKSHEETS

doc.save(ARTIFACTS_DIR + "XlsxSaveOptions.SelectionMode.xlsx", xlsx_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XlsxSaveOptions](../)

