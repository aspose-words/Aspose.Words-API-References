---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words XlsxDateTimeParsingMode-enum för effektiv textparsning av dokument. Identifiera enkelt datum- och tidsvärden i dina filer!
type: docs
weight: 6510
url: /sv/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Anger hur dokumenttext tolkas för att identifiera datum- och tidsvärden.

```csharp
public enum XlsxDateTimeParsingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| UseCurrentLocale | `0` | Datum- och tidsformatet som är inställt för den aktuella tråden används först för att analysera strängvärden. Om analyseringen misslyckas, provas andra vanliga datum- och tidsformat. |
| Auto | `1` | Datum- och tidsformatet som används i ett dokument bestäms automatiskt. Detta kan ta ytterligare tid. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
