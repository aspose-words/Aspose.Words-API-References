---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words för .NET
description: RtfSaveOptions ExportImagesForOldReaders fast egendom. Anger om nyckelorden för gamla läsare skrivs till RTF eller inte. Detta kan avsevärt påverka storleken på RTFdokumentet. Standardvärdet ärSann  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Anger om nyckelorden för "gamla läsare" skrivs till RTF eller inte. Detta kan avsevärt påverka storleken på RTF-dokumentet. Standardvärdet är`Sann` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Anmärkningar

"Gamla läsare" är pre-Microsoft Word 97-program och även WordPad. När detta alternativ är`Sann` Aspose.Words skriver ytterligare RTF-nyckelord. Dessa nyckelord gör att dokumentet kan visas korrekt när det öppnas i en "gammal läsare"-applikation, men kan avsevärt öka storleken på dokumentet.

Om du ställer in det här alternativet till`falsk`, då kommer endast bilder i WMF-, EMF- och BMP-format att visas i "gamla läsare".

## Exempel

Visar hur man sparar ett dokument till .rtf med anpassade alternativ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "RtfSaveOptions"-objekt för att skicka till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Ställ in egenskapen "ExportCompactSize" till "true" till
// minska storleken på det sparade dokumentet på bekostnad av höger-till-vänster-textkompatibilitet.
options.ExportCompactSize = true;

// Ställ in egenskapen "ExportImagesFotOldReaders" till "true" för att använda extra nyckelord för att säkerställa att vårt dokument är
// kompatibel med pre-Microsoft Word 97 läsare och WordPad.
// Ställ in egenskapen "ExportImagesFotOldReaders" till "false" för att minska storleken på dokumentet,
// men hindra gamla läsare från att kunna läsa eventuella icke-metafiler eller BMP-bilder som dokumentet kan innehålla.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Se även

* class [RtfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
