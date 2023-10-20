---
title: Section.Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words för .NET
description: Section Body fast egendom. ReturnerarBody barnnod för sektionen i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/section/body/
---
## Section.Body property

Returnerar[`Body`](../../body/) barnnod för sektionen.

```csharp
public Body Body { get; }
```

## Anmärkningar

[`Body`](../../body/) innehåller huvudtexten i avsnittet.

Returnerar`null` om avsnittet inte har en[`Body`](../../body/) nod bland sina barn.

## Exempel

Rensar huvudtexten från alla avsnitt från dokumentet och lämnar själva avsnitten.

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

// En sektion behöver en kropp som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Den här kroppen har inga barn, så vi kan inte lägga till körningar till den ännu.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Ring "EnsureMinimum" för att se till att den här texten innehåller minst ett tomt stycke.
body.EnsureMinimum();

// Nu kan vi lägga till körningar i brödtexten och få dokumentet att visa dem.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [Body](../../body/)
* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
