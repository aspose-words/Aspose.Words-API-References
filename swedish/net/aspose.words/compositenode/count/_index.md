---
title: CompositeNode.Count
second_title: Aspose.Words för .NET API Referens
description: CompositeNode fast egendom. Hämtar antalet omedelbara barn till denna nod.
type: docs
weight: 20
url: /sv/net/aspose.words/compositenode/count/
---
## CompositeNode.Count property

Hämtar antalet omedelbara barn till denna nod.

```csharp
public int Count { get; }
```

### Exempel

Visar hur man lägger till, uppdaterar och tar bort underordnade noder i en CompositeNodes samling av barn.

```csharp
Document doc = new Document();

// Ett tomt dokument har som standard ett stycke.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Sammansatta noder som vårt stycke kan innehålla andra sammansatta och infogade noder som underordnade.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Skapa ytterligare tre körnoder.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Dokumentets brödtext kommer inte att visa dessa körningar förrän vi infogar dem i en sammansatt nod
// som i sig är en del av dokumentets nodträd, som vi gjorde med den första körningen.
// Vi kan bestämma var textinnehållet i noder som vi infogar
// visas i dokumentet genom att ange en infogningsplats i förhållande till en annan nod i stycket.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Infoga den andra körningen i stycket framför den första körningen.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Infoga den tredje körningen efter den första körningen.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Infoga den första körningen till början av styckets samling av underordnade noder.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Vi kan ändra innehållet i körningen genom att redigera och ta bort befintliga underordnade noder.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Se även

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../compositenode/)
* hopsättning [Aspose.Words](../../../)


