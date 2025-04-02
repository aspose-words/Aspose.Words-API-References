---
title: XlsxSaveOptions.dateTimeParsingMode property
linktitle: dateTimeParsingMode property
articleTitle: dateTimeParsingMode property
second_title: Aspose.Words for NodeJs
description: "XlsxSaveOptions.dateTimeParsingMode property. Gets or sets the mode that specifies how document text is parsed to identify date and time values"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/xlsxsaveoptions/dateTimeParsingMode/
---

## XlsxSaveOptions.dateTimeParsingMode property

Gets or sets the mode that specifies how document text is parsed to identify date and time values.
The default value is [XlsxDateTimeParsingMode.UseCurrentLocale](../../xlsxdatetimeparsingmode/#UseCurrentLocale).



```js
get dateTimeParsingMode(): Aspose.Words.Saving.XlsxDateTimeParsingMode
```

### Examples

Shows how to specify autodetection of the date time format.

```js
let doc = new aw.Document(base.myDir + "Xlsx DateTime.docx");

let saveOptions = new aw.Saving.XlsxSaveOptions();
// Specify using datetime format autodetection.
saveOptions.dateTimeParsingMode = aw.Saving.XlsxDateTimeParsingMode.Auto;

doc.save(base.artifactsDir + "XlsxSaveOptions.dateTimeParsingMode.xlsx", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XlsxSaveOptions](../)

