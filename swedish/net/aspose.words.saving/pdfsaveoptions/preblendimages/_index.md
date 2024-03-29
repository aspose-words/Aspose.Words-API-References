---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words för .NET
description: PdfSaveOptions PreblendImages fast egendom. Hämtar eller ställer in ett värde som bestämmer om transparenta bilder ska förblandas med svart bakgrundsfärg i C#.
type: docs
weight: 260
url: /sv/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Hämtar eller ställer in ett värde som bestämmer om transparenta bilder ska förblandas med svart bakgrundsfärg.

```csharp
public bool PreblendImages { get; set; }
```

## Anmärkningar

Förblandning av bilder kan förbättra PDF-dokumentets visuella utseende i Adobe Reader och ta bort anti-aliasing-artefakter.

För att kunna visa förblandade bilder på rätt sätt måste PDF-visningsprogrammet stödja /Matte-inmatning i softmask-bildlexikon. Även förblandning av bilder kan minska PDF-renderingsprestanda.

Standardvärdet är`falsk`.

## Exempel

Visar hur du förblandar bilder med transparent bakgrund samtidigt som du sparar ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "PreblendImages" till "true" för att förblanda genomskinliga bilder
// med en bakgrund, vilket kan minska artefakter.
// Ställ in egenskapen "PreblendImages" till "false" för att återge transparenta bilder normalt.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Visar hur man förblandar bilder med transparent bakgrund (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "PreblendImages" till "true" för att förblanda genomskinliga bilder
// med en bakgrund, vilket kan minska artefakter.
// Ställ in egenskapen "PreblendImages" till "false" för att återge transparenta bilder normalt.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
