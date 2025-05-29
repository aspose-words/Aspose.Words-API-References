---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder CurrentStory-egenskapen för att effektivt komma åt och hantera den valda artikeln, vilket förbättrar din dokumentredigeringsupplevelse.
type: docs
weight: 70
url: /sv/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Hämtar berättelsen som för närvarande är vald i detta[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## Exempel

Visar hur man arbetar med en dokumentbyggares aktuella berättelse.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En berättelse är en typ av nod som har underordnade styckenoder, till exempel en brödtext.
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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
