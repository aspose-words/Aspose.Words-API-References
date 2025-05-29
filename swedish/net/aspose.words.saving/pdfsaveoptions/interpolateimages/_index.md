---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions InterpolateImages-egenskap, en viktig funktion som förbättrar bildkvaliteten i dina dokument. Optimera dina PDF-filer utan ansträngning!
type: docs
weight: 210
url: /sv/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

En flagga som anger om bildinterpolering ska utföras av en kompatibel läsare. När`falsk` är specificerad, skrivs inte flaggan till utdatadokumentet och används läsarens standardbeteende istället.

```csharp
public bool InterpolateImages { get; set; }
```

## Anmärkningar

När upplösningen för en källbild är betydligt lägre än utdataenhetens, täcker varje källprov många enhetspixlar. Som ett resultat kan bilder se ojämna eller blockiga ut. Dessa visuella artefakter kan minskas genom att tillämpa en bildinterpoleringsalgoritm under rendering. Istället för att måla alla pixlar som täcks av ett källprov med samma färg, försöker bildinterpolering skapa en smidig övergång mellan intilliggande provvärden.

En kompatibel läsare kan välja att inte implementera denna funktion i PDF, eller använda vilken specifik implementering av interpolering som helst.

Standardvärdet är`falsk`.

Interpoleringsflaggan är förbjuden enligt PDF/A-efterlevnad.`falsk` värdet kommer att användas automatically när du sparar till PDF/A.

## Exempel

Visar hur man utför interpolering på bilder när man sparar ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Sätt egenskapen "InterpolateImages" till "true" för att få läsaren som öppnar dokumentet att interpolera bilder.
// Deras upplösning bör vara lägre än den på enheten som visar dokumentet.
// Sätt egenskapen "InterpolateImages" till "false" för att läsaren inte ska använda någon interpolering.
saveOptions.InterpolateImages = interpolateImages;

// När vi öppnar det här dokumentet med en läsare som Adobe Acrobat måste vi zooma in på bilden
// för att se interpoleringseffekten om vi sparade dokumentet med den aktiverad.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
