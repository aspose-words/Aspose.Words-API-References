﻿---
title: XlsxSectionMode enumeration
linktitle: XlsxSectionMode enumeration
articleTitle: XlsxSectionMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.XlsxSectionMode enumeration. Specifies how sections are handled when saving a document in the XLSX format."
type: docs
weight: 930
url: /nodejs-net/aspose.words.saving/xlsxsectionmode/
---

## XlsxSectionMode enumeration

Specifies how sections are handled when saving a document in the XLSX format.


### Members

| Name | Description |
| --- | --- |
| MultipleWorksheets | Specifies that a separate worksheet is created for each section of a document. |
| SingleWorksheet | Specifies that all sections of a document are saved on one worksheet. |

### Examples

Shows how to save document as a separate worksheets.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

// Each section of a document will be created as a separate worksheet.
// Use 'SingleWorksheet' to display all document on one worksheet.
let xlsxSaveOptions = new aw.Saving.XlsxSaveOptions();
xlsxSaveOptions.sectionMode = aw.Saving.XlsxSectionMode.MultipleWorksheets;

doc.save(base.artifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

