---
title: PageSet.All
linktitle: All
articleTitle: All
second_title: Aspose.Words för .NET
description: Få tillgång till alla dokumentsidor i deras ursprungliga ordning med egenskapen PageSet All. Effektivisera ditt arbetsflöde och förbättra dokumenthanteringen utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/pageset/all/
---
## PageSet.All property

Hämtar en uppsättning med alla sidor i dokumentet i deras ursprungliga ordning.

```csharp
public static PageSet All { get; }
```

## Exempel

Visar hur man exporterar udda sidor från dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Nedan följer tre PageSet-egenskaper som vi kan använda för att filtrera bort en uppsättning sidor från
// vårt dokument för att spara i ett PDF-dokument baserat på pariteten hos deras sidnummer.
// 1 - Spara endast sidorna med jämna sidor:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Spara endast de udda sidorna:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Spara varje sida:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Se även

* class [PageSet](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
