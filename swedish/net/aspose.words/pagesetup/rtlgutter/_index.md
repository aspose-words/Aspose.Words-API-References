---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PageSetup RtlGutter i Microsoft Word optimerar sektionslayouter för höger-till-vänster- och vänster-till-höger-språk. Förbättra din dokumentdesign!
type: docs
weight: 380
url: /sv/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Hämtar eller anger om Microsoft Word använder marginaler för avsnittet baserat på ett höger-till-vänster-språk eller ett vänster-till-höger-språk.

```csharp
public bool RtlGutter { get; set; }
```

## Exempel

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

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
