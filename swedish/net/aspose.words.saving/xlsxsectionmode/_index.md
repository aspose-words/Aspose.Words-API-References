---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words XlsxSectionMode-enum optimerar dokumentsparning i XLSX-format, vilket förbättrar ditt arbetsflöde och din dokumenthantering.
type: docs
weight: 6530
url: /sv/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Anger hur avsnitt hanteras när ett dokument sparas i XLSX-format.

```csharp
public enum XlsxSectionMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| MultipleWorksheets | `0` | Anger att ett separat kalkylblad skapas för varje avsnitt i ett dokument. |
| SingleWorksheet | `1` | Anger att alla avsnitt i ett dokument sparas på ett kalkylblad. |

## Exempel

Visar hur man sparar dokument som separata kalkylblad.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Varje avsnitt i ett dokument skapas som ett separat kalkylblad.
// Använd 'SingleWorksheet' för att visa alla dokument på ett enda kalkylblad.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
