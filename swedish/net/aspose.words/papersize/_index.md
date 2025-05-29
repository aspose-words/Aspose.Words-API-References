---
title: PaperSize Enum
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PaperSize-enum för att definiera anpassade pappersstorlekar i dina dokument. Förbättra din dokumentformatering med lätthet!
type: docs
weight: 5110
url: /sv/net/aspose.words/papersize/
---
## PaperSize enumeration

Anger pappersstorlek.

```csharp
public enum PaperSize
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| A3 | `0` | 297 x 420 mm. |
| A4 | `1` | 210 x 297 mm. |
| A5 | `2` | 148 x 210 mm. |
| B4 | `3` | 250 x 353 mm. |
| B5 | `4` | 176 x 250 mm. |
| Executive | `5` | 7,25 x 10,5 tum. |
| Folio | `6` | 8,5 x 13 tum. |
| Ledger | `7` | 17 x 11 tum. |
| Legal | `8` | 8,5 x 14 tum. |
| Letter | `9` | 8,5 x 11 tum. |
| EnvelopeDL | `10` | 110 x 220 mm. |
| Quarto | `11` | 8,47 x 10,83 tum. |
| Statement | `12` | 8,5 x 5,5 tum. |
| Tabloid | `13` | 28 x 43 cm. |
| Paper10x14 | `14` | 25 x 38 cm. |
| Paper11x17 | `15` | 28 x 43 cm. |
| Number10Envelope | `16` | 4,125 x 9,5 tum. |
| JisB4 | `17` | 257 x 364 mm. |
| JisB5 | `18` | 182 x 257 mm. |
| Custom | `19` | Anpassad pappersstorlek. |

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

Visar hur man ställer in sidstorlekar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan ändra den aktuella sidans storlek till en fördefinierad storlek
// genom att använda egenskapen "PaperSize" i den här sektionens PageSetup-objekt.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Varje sektion har sitt eget PageSetup-objekt. När vi använder en dokumentbyggare för att skapa en ny sektion,
// den sektionens PageSetup-objekt ärver alla värden från föregående sektions PageSetup-objekt.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Ange en anpassad storlek för sidorna i det här avsnittet.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

Visar hur man konstruerar ett Aspose.Words-dokument för hand.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan barn.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta undernoder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla i dess nodsamling igen.
// Skapa först en ny sektion och lägg sedan till den som ett underordnat avsnitt till rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// Ange vissa sidinställningar för avsnittet.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// En sektion behöver en brödtext, som innehåller och visar allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Skapa ett stycke, ange några formateringsegenskaper och lägg sedan till det som ett underordnat stycke i brödtexten.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Slutligen, lägg till lite innehåll för att göra dokumentet. Skapa en körning,
// ange dess utseende och innehåll och lägg sedan till det som ett underordnat stycke.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
