---
title: XlsxSaveOptions.sectionMode property
linktitle: sectionMode property
articleTitle: sectionMode property
second_title: Aspose.Words for NodeJs
description: "XlsxSaveOptions.sectionMode property. Gets or sets the way how sections are handled when saving to the output XLSX document"
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Saving/xlsxsaveoptions/sectionMode/
---

## XlsxSaveOptions.sectionMode property

Gets or sets the way how sections are handled when saving to the output XLSX document.
The default value is [XlsxSectionMode.MultipleWorksheets](../../xlsxsectionmode/#MultipleWorksheets).



```js
get sectionMode(): Aspose.Words.Saving.XlsxSectionMode
```

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

* module [Aspose.Words.Saving](../../)
* class [XlsxSaveOptions](../)

