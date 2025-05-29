---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen XlsxSaveOptions SectionMode optimerar sektionshanteringen för XLSX-exporter, vilket säkerställer sömlös dokumenthantering och flera kalkylblad.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Hämtar eller anger hur avsnitt hanteras när de sparas till XLSX-utdatadokumentet. Standardvärdet ärMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
