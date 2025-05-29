---
title: CompositeNode.PrependChild
linktitle: PrependChild
articleTitle: PrependChild
second_title: Aspose.Words för .NET
description: Upptäck hur metoden CompositeNode PrependChild förbättrar din datastruktur genom att effektivt lägga till noder i början av din lista över underordnade noder.
type: docs
weight: 170
url: /sv/net/aspose.words/compositenode/prependchild/
---
## CompositeNode.PrependChild&lt;T&gt; method

Lägger till den angivna noden i början av listan över underordnade noder för denna nod.

```csharp
public T PrependChild<T>(T newChild)
    where T : Node
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| newChild | T | Noden som ska läggas till. |

### Returvärde

Noden tillagd.

## Anmärkningar

Om*newChild* redan finns i trädet, tas det först bort.

Om noden som infogas skapades från ett annat dokument bör du använda [`ImportNode`](../../documentbase/importnode/) för att importera noden till det aktuella dokumentet. Den importerade noden kan sedan infogas i det aktuella dokumentet.

## Exempel

Visar hur man lägger till, uppdaterar och tar bort underordnade noder i en CompositeNodes samling av underordnade noder.

```csharp
Document doc = new Document();

// Ett tomt dokument har som standard ett stycke.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Sammansatta noder som vårt stycke kan innehålla andra sammansatta och inline-noder som underordnade.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Skapa ytterligare tre körnoder.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Dokumentets innehåll kommer inte att visa dessa körningar förrän vi infogar dem i en sammansatt nod
// som i sig är en del av dokumentets nodträd, precis som vi gjorde med den första körningen.
// Vi kan avgöra var textinnehållet i noder som vi infogar ska
// visas i dokumentet genom att ange en insättningsplats i förhållande till en annan nod i stycket.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Infoga den andra satsen i stycket före den första satsen.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Infoga den tredje körningen efter den första körningen.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Infoga den första körningen i början av styckets samling av underordnade noder.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Vi kan ändra innehållet i körningen genom att redigera och ta bort befintliga undernoder.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Se även

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
