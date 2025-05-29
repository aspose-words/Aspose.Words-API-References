---
title: PageSetup.MultiplePages
linktitle: MultiplePages
articleTitle: MultiplePages
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen Sidinställningar Flera sidor optimerar dokumentutskrift för sömlös häftesbindning. Förbättra dina flersidiga dokument idag!
type: docs
weight: 270
url: /sv/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

För dokument med flera sidor, hämtar eller anger hur ett dokument skrivs ut eller renderas så att det kan bindas som ett häfte.

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

## Exempel

Visar hur man konfigurerar ett dokument som kan skrivas ut som en bokvikning.

```csharp
Document doc = new Document();

// Infoga text som sträcker sig över 16 sidor.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurera den första sektionens "PageSetup"-egenskap för att skriva ut dokumentet i form av en bokvikning.
// När vi skriver ut detta dokument på båda sidor kan vi ta sidorna och stapla dem
// och vik dem alla på mitten samtidigt. Innehållet i dokumentet kommer att radas upp till en bokvikning.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Vi kan bara ange antalet ark i multiplar av 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Visar hur man ställer in fästmarginaler.

```csharp
Document doc = new Document();

// Infoga text som sträcker sig över flera sidor.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// En mellanrumsränna lägger till mellanslag i antingen vänster eller höger sidmarginal,
// vilket kompenserar för att mittvikningen av sidor i en bok inkräktar på sidans layout.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Bestäm hur mycket utrymme våra sidor har för text inom marginalerna och lägg sedan till ett visst utrymme för att utfylla marginalen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Sätt egenskapen "RtlGutter" till "true" för att placera fästringen i en mer lämplig position för text från höger till vänster.
pageSetup.RtlGutter = true;

// Ställ in egenskapen "MultiplePages" till "MultiplePagesType.MirrorMargins" för att alternera
// vänster/höger sidposition för marginalerna på varje sida.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Se även

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
