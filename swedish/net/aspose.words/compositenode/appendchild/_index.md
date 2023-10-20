---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words för .NET
description: CompositeNode AppendChild metod. Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod i C#.
type: docs
weight: 60
url: /sv/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild method

Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod.

```csharp
public Node AppendChild(Node newChild)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| newChild | Node | Noden att lägga till. |

### Returvärde

Noden tillagd.

## Anmärkningar

Om*newChild* redan finns i trädet tas den först bort.

Om noden som infogas skapades från ett annat dokument bör du använda [`ImportNode`](../../documentbase/importnode/) för att importera noden till det aktuella dokumentet. Den importerade noden kan sedan infogas i det aktuella dokumentet.

## Exempel

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

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
