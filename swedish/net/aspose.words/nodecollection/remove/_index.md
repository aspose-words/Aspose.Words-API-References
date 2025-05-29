---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Ta enkelt bort noder från ditt dokument med NodeCollection Remove-metoden, vilket effektiviserar din datahantering och förbättrar prestandan.
type: docs
weight: 90
url: /sv/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

Tar bort noden från samlingen och från dokumentet.

```csharp
public void Remove(Node node)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| node | Node | Noden som ska tas bort. |

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
