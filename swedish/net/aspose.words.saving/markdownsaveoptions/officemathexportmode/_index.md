---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MarkdownSaveOptions OfficeMathExportMode för att anpassa OfficeMath-utdata. Optimera dina filer med flexibla exportinställningar!
type: docs
weight: 120
url: /sv/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

Anger hur OfficeMath ska skrivas till utdatafilen. Standardvärdet ärText .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Exempel

Visar hur OfficeMath kommer att skrivas till dokumentet.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Se även

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
