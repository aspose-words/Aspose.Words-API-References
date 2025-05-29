---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words för .NET
description: Upptäck hur NodeCollection Contains-metoden effektivt kontrollerar om en nod finns i din samling, vilket förbättrar dina datahanteringsmöjligheter.
type: docs
weight: 50
url: /sv/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

Avgör om en nod finns i samlingen.

```csharp
public bool Contains(Node node)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| node | Node | Noden som ska lokaliseras. |

### Returvärde

`sann`om föremålet finns i samlingen; annars,`falsk`.

## Anmärkningar

Denna metod utför en linjär sökning; därför är den genomsnittliga exekveringstiden proportionell mot[`Count`](../count/).

## Exempel

Visar hur man arbetar med en NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till text i dokumentet genom att infoga Runs med hjälp av en DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Varje anrop av metoden "Write" skapar en ny Run,
// som sedan visas i det överordnade styckets RunCollection.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Vi kan också infoga en nod i RunCollection manuellt.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Få åtkomst till enskilda körningar och ta bort dem för att ta bort deras text från dokumentet.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Se även

* class [Node](../../node/)
* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
