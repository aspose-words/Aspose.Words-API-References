---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till specifika avsnitt med egenskapen SectionCollection Item. Hämta valfritt avsnitt via index för effektiv datahantering.
type: docs
weight: 10
url: /sv/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Hämtar ett avsnitt vid det angivna indexet.

```csharp
public Section this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index till listan över avsnitt. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

## Exempel

Visar när dokumentets sidlayout ska beräknas om.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Att spara ett dokument till PDF, som en bild eller skriva ut för första gången kommer automatiskt
// cachelagrar dokumentets layout inom dess sidor.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Ändra dokumentet på något sätt.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// I den nuvarande versionen av Aspose.Words återskapas inte dokumentet automatiskt när du ändrar det
// den cachade sidlayouten. Om vi önskar den cachade layouten
// för att hålla oss uppdaterade måste vi uppdatera den manuellt.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Visar hur man förbereder en ny sektionsnod för redigering.

```csharp
Document doc = new Document();

// Ett tomt dokument kommer med ett avsnitt, som har en brödtext, som i sin tur har ett stycke.
// Vi kan lägga till innehåll i det här dokumentet genom att lägga till element som textsekvenser, former eller tabeller i stycket.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Om vi lägger till en ny sektion som denna, kommer den inte att ha någon brödtext eller några andra underordnade noder.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Kör metoden "EnsureMinimum" för att lägga till en brödtext och ett stycke i det här avsnittet för att börja redigera det.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [Section](../../section/)
* class [SectionCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
