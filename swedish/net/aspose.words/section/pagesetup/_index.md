---
title: Section.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup för anpassningsbara avsnittsinställningar. Optimera din dokumentlayout med enkel åtkomst till sid- och avsnittskonfigurationer.
type: docs
weight: 50
url: /sv/net/aspose.words/section/pagesetup/
---
## Section.PageSetup property

Returnerar ett objekt som representerar sidinställningar och sektionsegenskaper.

```csharp
public PageSetup PageSetup { get; }
```

## Exempel

Visar hur man skapar en bred blå kantlinje högst upp på första sidan.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
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

* class [PageSetup](../../pagesetup/)
* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
