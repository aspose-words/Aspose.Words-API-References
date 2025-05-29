---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words för .NET
description: Upptäck XlsxSaveOptions DateTimeParsingMode-egenskap för att anpassa hur ditt dokument tolkar datum och tider, vilket säkerställer korrekt datatolkning.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Hämtar eller ställer in läget som anger hur dokumenttext tolkas för att identifiera datum- och tidsvärden. Standardvärdet ärUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

## Exempel

Visar hur man anger automatisk detektering av datum- och tidsformat.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Ange med hjälp av automatisk detektion i datum- och tidsformat.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Se även

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
