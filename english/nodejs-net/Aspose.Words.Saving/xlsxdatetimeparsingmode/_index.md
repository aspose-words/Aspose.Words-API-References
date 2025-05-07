---
title: XlsxDateTimeParsingMode enumeration
linktitle: XlsxDateTimeParsingMode enumeration
articleTitle: XlsxDateTimeParsingMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.XlsxDateTimeParsingMode enumeration. Specifies how document text is parsed to identify date and time values."
type: docs
weight: 900
url: /nodejs-net/aspose.words.saving/xlsxdatetimeparsingmode/
---

## XlsxDateTimeParsingMode enumeration

Specifies how document text is parsed to identify date and time values.


### Members

| Name | Description |
| --- | --- |
| UseCurrentLocale | The datetime format set for the current thread is used first to parse string values. If the parsing fails, other common datetime formats are tried. |
| Auto | The datetime format used in a document is determined automatically. This may take additional time. |

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

* module [Aspose.Words.Saving](../)

