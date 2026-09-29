---
title: XlsxSectionMode enumeration
linktitle: XlsxSectionMode enumeration
articleTitle: XlsxSectionMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.XlsxSectionMode enumeration. Specifies how sections are handled when saving a document in the XLSX format."
type: docs
weight: 970
url: /it/python-net/aspose.words.saving/xlsxsectionmode/
---

## XlsxSectionMode enumeration

Specifies how sections are handled when saving a document in the XLSX format.


### Members

| Name | Description |
| --- | --- |
| MULTIPLE_WORKSHEETS | Specifies that a separate worksheet is created for each section of a document. |
| SINGLE_WORKSHEET | Specifies that all sections of a document are saved on one worksheet. |

### Examples

Shows how to save document as a separate worksheets.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
# Ognuna sezione di un documento verrà creata come un foglio di lavoro separato.
# Usa 'SingleWorksheet' per visualizzare tutto il documento su un unico foglio di lavoro.
xlsx_save_options = aw.saving.XlsxSaveOptions()
xlsx_save_options.section_mode = aw.saving.XlsxSectionMode.MULTIPLE_WORKSHEETS
doc.save(file_name=ARTIFACTS_DIR + 'XlsxSaveOptions.SelectionMode.xlsx', save_options=xlsx_save_options)
```

### See Also

* module [aspose.words.saving](../)

