---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions egenskap PreblendImages. Kontrollera enkelt transparent bildblandning för förbättrad dokumentkvalitet och visuell attraktionskraft.
type: docs
weight: 270
url: /sv/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Hämtar eller ställer in ett värde som avgör om transparenta bilder ska förblandas med svart bakgrundsfärg.

```csharp
public bool PreblendImages { get; set; }
```

## Anmärkningar

Förblandning av bilder kan förbättra PDF-dokumentets utseende i Adobe Reader och ta bort kantutjämningsartefakter.

För att kunna visa förblandade bilder korrekt måste PDF-visningsprogrammet stödja /Matte-inmatning i soft-mask-bildordboken. Även förblandning av bilder kan försämra PDF-renderingsprestanda.

Standardvärdet är`falsk`.

## Exempel

Visar hur man förblandar bilder med genomskinliga bakgrunder när man sparar ett dokument som PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Sätt egenskapen "PreblendImages" till "true" för att förblanda transparenta bilder
// med en bakgrund, vilket kan minska artefakter.
// Sätt egenskapen "PreblendImages" till "false" för att rendera transparenta bilder normalt.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
