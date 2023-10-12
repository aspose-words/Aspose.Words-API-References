---
title: XpsSaveOptions.OutlineOptions
second_title: Aspose.Words för .NET API Referens
description: XpsSaveOptions fast egendom. Gör det möjligt att ange konturalternativ.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Gör det möjligt att ange konturalternativ.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Anmärkningar

Anteckna det[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) alternativet fungerar inte när du sparar till XPS.

### Exempel

Visar hur man begränsar rubrikernas nivå som visas i konturerna av ett sparat XPS-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som TOC-poster på nivåerna 1, 2 och sedan 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// XPS-dokumentet kommer att innehålla en disposition, en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Genom att klicka på en post i denna disposition kommer vi till platsen för dess respektive rubrik.
// Ställ in egenskapen "HeadingsOutlineLevels" till "2" för att utesluta alla rubriker vars nivåer är över 2 från dispositionen.
// De två sista rubrikerna vi har infogat ovan kommer inte att visas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Se även

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../xpssaveoptions/)
* hopsättning [Aspose.Words](../../../)


