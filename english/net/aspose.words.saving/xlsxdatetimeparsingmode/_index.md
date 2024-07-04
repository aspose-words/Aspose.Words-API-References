---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.XlsxDateTimeParsingMode enum. Specifies how document text is parsed to identify date and time values in C#.
type: docs
weight: 6000
url: /net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Specifies how document text is parsed to identify date and time values.

```csharp
public enum XlsxDateTimeParsingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| UseCurrentLocale | `0` | The datetime format set for the current thread is used first to parse string values. If the parsing fails, other common datetime formats are tried. |
| Auto | `1` | The datetime format used in a document is determined automatically. This may take additional time. |

## Examples

Shows how to specify autodetection of the date time format.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Specify using datetime format autodetection.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
