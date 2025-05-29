---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words för .NET
description: Optimera dina PDF-filer med PdfSaveOptions! Kontrollera teckensnittsersättning för TrueType-teckensnitt som Arial och Times New Roman för att förbättra dokumentkvaliteten.
type: docs
weight: 330
url: /sv/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Hämtar eller anger ett värde som avgör om TrueType-teckensnitten Arial, Times New Roman, Courier New och Symbol ska ersättas med kärn-PDF Type 1-teckensnitt.

```csharp
public bool UseCoreFonts { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` När detta värde är inställt på`sann` Typsnitten Arial, Times New Roman, Courier New och Symbol ersätts i PDF-dokumentet med motsvarande kärntypsnitt av typ 1.

Kärnteckensnitt i PDF-format, eller deras teckensnittsvärden och lämpliga ersättningsteckensnitt, måste vara tillgängliga för alla PDF-visningsprogram.

Den här inställningen fungerar endast för text i ANSI-kodning (Windows-1252). Text som inte är ANSI kommer att skrivas med inbäddat TrueType-teckensnitt oavsett den här inställningen.

PDF/A- och PDF/UA-efterlevnad kräver att alla teckensnitt är inbäddade.`falsk` Värdet kommer att användas automatiskt när man sparar till PDF/A och PDF/UA.

Kärnteckensnitt stöds inte när man sparar i PDF 2.0-format.`falsk` Värdet kommer att användas automatiskt när du sparar till PDF 2.0.

Det här alternativet har högre prioritet än[`FontEmbeddingMode`](../fontembeddingmode/) alternativ.

## Exempel

Visar hur man aktiverar/inaktiverar PDF Type 1-teckensnittsersättning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Sätt egenskapen "UseCoreFonts" till "true" för att ersätta vissa teckensnitt,
// inklusive de två teckensnitten i vårt dokument, med deras PDF Typ 1-motsvarigheter.
// Sätt egenskapen "UseCoreFonts" till "false" för att inte tillämpa PDF Type 1-teckensnitt.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
