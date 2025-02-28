---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words for .NET
description: Discover XlsxSaveOptions' DateTimeParsingMode property to customize how your document parses dates and times, ensuring accurate data interpretation.
type: docs
weight: 30
url: /net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Gets or sets the mode that specifies how document text is parsed to identify date and time values. The default value is UseCurrentLocale.

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

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

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
