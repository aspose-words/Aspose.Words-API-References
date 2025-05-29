---
title: Section
linktitle: Section
articleTitle: Section
second_title: Aspose.Words för .NET
description: Skapa dynamiska webbsektioner enkelt med vår Section Constructor. Initiera och anpassa enkelt din Section-klass för optimal webbplatsprestanda.
type: docs
weight: 10
url: /sv/net/aspose.words/section/section/
---
## Section constructor

Initierar en ny instans av Section-klassen.

```csharp
public Section(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

## Anmärkningar

När avsnittet skapas tillhör det det angivna dokumentet, men är ännu inte en del av dokumentet och[`ParentNode`](../../node/parentnode/) är`null`.

Att inkludera[`Section`](../) i ett dokumentanvändning[`InsertAfter`](../../compositenode/insertafter/) och [`InsertBefore`](../../compositenode/insertbefore/) metoderna för[`Document`](../../document/) ELLER [`Add`](../../nodecollection/add/) och[`Insert`](../../nodecollection/insert/) metoderna för[`Sections`](../../document/sections/) egendom.

## Exempel

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

* class [DocumentBase](../../documentbase/)
* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
