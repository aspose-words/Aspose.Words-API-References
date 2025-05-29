---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words för .NET
description: Optimera dina RTF-dokument med egenskapen ExportImagesForOldReaders. Kontrollera inkludering av nyckelord för äldre läsare, vilket påverkar filstorlek och prestanda.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Anger om nyckelorden för "gamla läsare" skrivs till RTF eller inte. Detta kan påverka storleken på RTF-dokumentet avsevärt. Standardvärdet är`sann` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Anmärkningar

"Gamla läsare" är program som är äldre än Microsoft Word 97 och även WordPad. När det här alternativet är aktiverat`sann` Aspose.Words skriver ytterligare RTF-nyckelord. Dessa nyckelord gör att dokumentet visas korrekt när det öppnas i ett "gammalt läsarprogram", men kan öka dokumentets storlek avsevärt.

Om du ställer in det här alternativet på`falsk`då kommer endast bilder i WMF-, EMF- och BMP-format att visas i "gamla läsare".

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

* class [RtfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
