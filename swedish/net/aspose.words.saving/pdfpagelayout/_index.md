---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.PdfPageLayout-enum för optimal PDF-visning. Anpassa sidlayouter för förbättrad läsbarhet i alla PDF-läsare.
type: docs
weight: 6290
url: /sv/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Anger vilken sidlayout som ska användas när dokumentet öppnas i en PDF-läsare.

```csharp
public enum PdfPageLayout
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| SinglePage | `0` | Visa en sida i taget. |
| OneColumn | `1` | Visa sidorna i en kolumn. |
| TwoColumnLeft | `2` | Visa sidorna i två kolumner, med udda sidor till vänster. |
| TwoColumnRight | `3` | Visa sidorna i två kolumner, med udda sidor till höger. |
| TwoPageLeft | `4` | Visar sidorna två åt gången, med udda sidor till vänster. |
| TwoPageRight | `5` | Visa sidorna två åt gången, med udda sidor till höger. |

## Exempel

Visar hur sidor visas när de öppnas i en PDF-läsare.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Visa sidorna två åt gången, med udda sidor till vänster.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
