---
title: DocumentBuilder.CurrentStory
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder fast egendom. Hämtar berättelsen som för närvarande är vald i denna DocumentBuilder.
type: docs
weight: 70
url: /sv/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Hämtar berättelsen som för närvarande är vald i denna DocumentBuilder.

```csharp
public Story CurrentStory { get; }
```

### Exempel

Visar hur man arbetar med en dokumentbyggares aktuella historia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En berättelse är en typ av nod som har underordnade paragrafnoder, till exempel en Kropp.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// En berättelse kan också innehålla tabeller.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Se även

* class [Story](../../story/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


