---
title: DocumentBuilder.PageSetup
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder fast egendom. Returnerar ett objekt som representerar aktuell siduppsättning och avsnittsegenskaper.
type: docs
weight: 160
url: /sv/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Returnerar ett objekt som representerar aktuell siduppsättning och avsnittsegenskaper.

```csharp
public PageSetup PageSetup { get; }
```

### Exempel

Visar hur man tillämpar och återställer sidinställningar till avsnitt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändra sidinställningarna för byggarens nuvarande avsnitt och lägg till text.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Om vi startar ett nytt avsnitt med hjälp av en dokumentbyggare,
// det kommer att ärva byggarens nuvarande sidinställningar.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Vi kan återställa dess sidinställningar till deras standardvärden med "ClearFormatting"-metoden.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Se även

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


