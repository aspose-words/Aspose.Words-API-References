---
title: Orientation Enum
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Orientation-enum för sömlös kontroll över sidorientering. Förbättra din dokumentformatering med enkelhet och precision!
type: docs
weight: 5050
url: /sv/net/aspose.words/orientation/
---
## Orientation enumeration

Anger sidorientering.

```csharp
public enum Orientation
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Portrait | `1` | Stående sidorientering (smal och hög). |
| Landscape | `2` | Liggande sidorientering (bred och kort). |

## Exempel

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
