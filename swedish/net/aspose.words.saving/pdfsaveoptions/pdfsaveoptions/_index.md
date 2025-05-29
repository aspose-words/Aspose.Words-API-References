---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions-konstruktorn, utformad för att enkelt initiera och spara dina dokument i högkvalitativt PDF-format. Effektivisera ditt arbetsflöde idag!
type: docs
weight: 10
url: /sv/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument i Pdf format.

```csharp
public PdfSaveOptions()
```

## Exempel

Visar hur man aktiverar eller inaktiverar delmängd vid inbäddning av teckensnitt när ett dokument renderas till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Konfigurera våra teckensnittskällor för att säkerställa att vi har tillgång till båda teckensnitten i det här dokumentet.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Eftersom vårt dokument innehåller ett anpassat teckensnitt kan det vara önskvärt att bädda in det i utdatadokumentet.
// Sätt egenskapen "EmbedFullFonts" till "true" för att bädda in alla teckensnitt i varje inbäddat teckensnitt i PDF-filen.
// Dokumentets storlek kan bli mycket stor, men vi kommer att kunna använda alla teckensnitt fullt ut om vi redigerar PDF-filen.
// Sätt egenskapen "EmbedFullFonts" till "false" för att tillämpa delmängder på teckensnitt och spara endast tecknen
// som dokumentet använder. Filen kommer att vara betydligt mindre,
// men vi kan behöva åtkomst till anpassade teckensnitt om vi redigerar dokumentet.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
