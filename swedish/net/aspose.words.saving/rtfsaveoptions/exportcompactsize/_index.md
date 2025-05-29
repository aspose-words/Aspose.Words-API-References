---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words för .NET
description: Optimera RTF-dokumentstorleken med egenskapen ExportCompactSize. Säkerställ effektiv lagring samtidigt som textintegriteten bibehålls, även med RTF-innehåll.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Gör det möjligt att göra RTF-dokument mindre i storlek, men om de innehåller RTL-text (höger-till-vänster) kommer den inte att visas korrekt. Standardvärdet är`falsk` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Anmärkningar

Om dokumentet som du vill konvertera till RTF med Aspose.Words inte innehåller höger-till-vänster-text på språk som arabiska, kan du ställa in det här alternativet på`sann` för att minska storleken på den resulterande RTF-filen.

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
