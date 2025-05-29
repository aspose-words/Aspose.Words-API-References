---
title: XpsSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OutlineOptions i XpsSaveOptions för att anpassa dokumentets dispositionsinställningar för förbättrad organisation och presentation.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Gör det möjligt att ange dispositionsalternativ.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Anmärkningar

Observera att[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) Alternativet fungerar inte när du sparar till XPS.

## Exempel

Visar hur man begränsar rubriknivån som visas i dispositionen i ett sparat XPS-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som innehållsförteckningsposter för nivå 1, 2 och sedan 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Det utgående XPS-dokumentet kommer att innehålla en disposition, en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "2" för att exkludera alla rubriker vars nivåer är över 2 från dispositionen.
// De två sista rubrikerna som vi har infogat ovan kommer inte att visas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Se även

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
