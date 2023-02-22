---
title: ParagraphFormat.Alignment
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar eller ställer in textjustering för stycket.
type: docs
weight: 30
url: /sv/net/aspose.words/paragraphformat/alignment/
---
## ParagraphFormat.Alignment property

Hämtar eller ställer in textjustering för stycket.

```csharp
public ParagraphAlignment Alignment { get; set; }
```

### Exempel

Visar hur man infogar ett stycke i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// "Writeln"-metoden avslutar stycket efter att ha lagt till text
// och startar sedan en ny rad och lägger till ett nytt stycke.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

Visar hur man konstruerar ett Aspose.Words-dokument för hand.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan underordnade.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta underordnade noder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla på dess nodsamling.
// Skapa först ett nytt avsnitt och lägg sedan till det som ett underordnat dokument i rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// Ställ in några sidinställningar för avsnittet.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// En sektion behöver en kropp som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Skapa ett stycke, ange några formateringsegenskaper och lägg sedan till det som ett underordnat stycke i brödtexten.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Slutligen, lägg till lite innehåll för att göra dokumentet. Skapa en löprunda,
// ställ in dess utseende och innehåll och lägg sedan till det som ett barn till stycket.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Se även

* enum [ParagraphAlignment](../../paragraphalignment/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


