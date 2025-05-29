---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words för .NET
description: Upptäck hur funktionen PdfSaveOptions EmbedFullFonts förbättrar dina PDF-dokument genom att säkerställa fullständig teckensnittsinbäddning för perfekt formatering.
type: docs
weight: 120
url: /sv/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Styr hur teckensnitt bäddas in i de resulterande PDF-dokumenten.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`, vilket innebär att teckensnitten delmängderas innan de bäddas in. Delmängdsinställning är användbar om du vill hålla utdatafilens storlek mindre. Delmängdsinställning tar bort alla oanvända tecken från ett teckensnitt.

När detta värde är inställt på`sann`, en komplett teckensnittsfil bäddas in i PDF-filen utan delmängd. Detta kommer att resultera i större utdatafiler, men kan vara ett användbart alternativ när du vill redigera den resulterande PDF-filen senare (t.ex. lägga till mer text).

Vissa teckensnitt är stora (flera megabyte) och att bädda in dem utan subsetting kommer att resultera i stora utdatadokument.

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
