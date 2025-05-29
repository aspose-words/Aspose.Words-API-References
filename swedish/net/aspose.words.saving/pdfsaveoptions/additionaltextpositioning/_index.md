---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words för .NET
description: Upptäck egenskapen AdditionalTextPositioning i PdfSaveOptions för att styra textpositionering i PDF-filer. Förbättra dokumentets layout utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

En flagga som anger om ytterligare textpositioneringsoperatorer ska skrivas eller inte.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Anmärkningar

Om`sann` , ytterligare textpositioneringsoperatorer skrivs till utdata-PDF:en. Detta kan bidra till att övervinna problem med felaktig textpositionering med vissa skrivare. Nackdelen är den ökade PDF-dokumentstorleken.

Standardvärdet är`falsk`.

## Exempel

Visa hur man skriver ytterligare textpositioneringsoperatorer.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Sätt egenskapen "AdditionalTextPositioning" till "true" för att försöka korrigera felaktiga
    // elementpositionering i utdata-PDF:en, om det finns någon, på bekostnad av ökad filstorlek.
    // Sätt egenskapen "AdditionalTextPositioning" till "false" för att rendera dokumentet som vanligt.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
