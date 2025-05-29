---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RtfSaveOptions SaveFormat för att enkelt spara dina dokument i RTF-format, vilket säkerställer kompatibilitet och enkel delning.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exempel

Visar hur man sparar ett dokument till .rtf med anpassade alternativ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "RtfSaveOptions"-objekt som ska skickas till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF-fil.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Sätt egenskapen "ExportCompactSize" till "true" för att
// minska storleken på det sparade dokumentet på bekostnad av textkompatibilitet från höger till vänster.
options.ExportCompactSize = true;

// Sätt egenskapen "ExportImagesFotOldReaders" till "true" för att använda extra nyckelord för att säkerställa att vårt dokument är
// kompatibel med läsare och WordPad före Microsoft Word 97.
// Sätt egenskapen "ExportImagesFotOldReaders" till "false" för att minska dokumentets storlek,
// men förhindra att gamla läsare kan läsa eventuella icke-metafiler eller BMP-bilder som dokumentet kan innehålla.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
