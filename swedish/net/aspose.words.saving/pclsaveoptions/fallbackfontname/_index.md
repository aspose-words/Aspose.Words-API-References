---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PclSaveOptions FallbackFontName som säkerställer sömlös utskrift med ett standardteckensnitt när önskat teckensnitt inte är tillgängligt.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Namn på det teckensnitt som ska användas om inget förväntat teckensnitt hittas i skrivarens och de inbyggda teckensnittssamlingarna.

```csharp
public string FallbackFontName { get; set; }
```

## Anmärkningar

Om ingen reservfunktion hittas genereras en varning och teckensnittet "Arial" används.

## Exempel

Visar hur man deklarerar ett teckensnitt som en skrivare kommer att använda på utskriven text som ersättning om dess ursprungliga teckensnitt inte är tillgängligt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Detta dokument instruerar tryckeriet att använda "Times New Roman" på texten med det saknade teckensnittet.
// Om "Times New Roman" inte heller är tillgängligt, kommer skrivaren att använda teckensnittet "Arial" som standard.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Se även

* class [PclSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
