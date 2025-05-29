---
title: PageSetup.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words för .NET
description: Upptäck orienteringsfunktionen i PageSetup för att enkelt justera dokumentets sidlayout. Optimera din utskrift med anpassningsbara orienteringsinställningar!
type: docs
weight: 290
url: /sv/net/aspose.words/pagesetup/orientation/
---
## PageSetup.Orientation property

Returnerar eller anger sidans orientering.

```csharp
public Orientation Orientation { get; set; }
```

## Anmärkningar

Skiftande`Orientation` byten[`PageWidth`](../pagewidth/) och[`PageHeight`](../pageheight/).

## Exempel

Visar hur man justerar pappersstorlek, orientering, marginaler och andra inställningar för ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Visar hur man tillämpar och återställer inställningar för sidinställningar för avsnitt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändra sidinställningarna för den aktuella sektionen i skaparen och lägg till text.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Om vi startar ett nytt avsnitt med hjälp av en dokumentbyggare,
// den kommer att ärva skaparens nuvarande sidinställningar.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Vi kan återställa dess sidinställningar till standardvärdena med hjälp av metoden "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Se även

* enum [Orientation](../../orientation/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
