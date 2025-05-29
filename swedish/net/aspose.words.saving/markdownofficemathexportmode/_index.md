---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.MarkdownOfficeMathExportMode förbättrar exporten av OfficeMath till Markdown, vilket säkerställer korrekt och effektiv dokumentkonvertering.
type: docs
weight: 6050
url: /sv/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Anger hur Aspose.Words exporterar OfficeMath till Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | `0` | Exportera OfficeMath som vanlig text. |
| Image | `1` | Exportera OfficeMath som bild. |
| MathML | `2` | Exportera OfficeMath som MathML. |

## Exempel

Visar hur OfficeMath kommer att skrivas till dokumentet.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
