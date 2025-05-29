---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words för .NET
description: Styr din dokumentrendering med FixedPageSaveOptions PageSet. Välj enkelt specifika sidor eller välj alla för sömlös utskrift. Optimera ditt arbetsflöde!
type: docs
weight: 70
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Hämtar eller ställer in sidorna som ska renderas. Standard är alla sidor i dokumentet.

```csharp
public PageSet PageSet { get; set; }
```

## Exempel

Visar hur man extraherar sidor baserat på exakta sidindex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till fem sidor i dokumentet.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Skapa ett "XpsSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Använd egenskapen "PageSet" för att välja en uppsättning av dokumentets sidor som ska sparas för att skapa XPS-utdata.
// I det här fallet väljer vi, via ett nollbaserat index, endast tre sidor: sida 1, sida 2 och sida 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Visar hur man konverterar endast vissa sidor i ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur den metoden konverterar dokumentet till .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Sätt "PageIndex" till "1" för att rendera en del av dokumentet med början från den andra sidan.
    options.PageSet = new PageSet(1);

    // Detta dokument kommer att innehålla en sida med början från sida två, som bara kommer att innehålla den andra sidan.
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
