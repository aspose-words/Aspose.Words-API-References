---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Upptäck NodeCollection Add-metoden för att enkelt lägga till noder i din samling, vilket förbättrar din datahantering med enkelhet och effektivitet.
type: docs
weight: 30
url: /sv/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Lägger till en nod i slutet av samlingen.

```csharp
public void Add(Node node)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| node | Node | Noden som ska läggas till i slutet av samlingen. |

### Undantag

| undantag | skick |
| --- | --- |
| NotSupportedException | De[`NodeCollection`](../) är en "djup" samling. |

## Anmärkningar

Noden infogas som ett underordnat objekt i nodobjektet från vilket samlingen skapades.

Om noden som infogas skapades från ett annat dokument bör du använda [`ImportNode`](../../documentbase/importnode/) för att importera noden till det aktuella dokumentet. Den importerade noden kan sedan infogas i det aktuella dokumentet.

## Exempel

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

* class [Node](../../node/)
* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
