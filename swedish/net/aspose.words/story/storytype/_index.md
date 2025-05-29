---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words för .NET
description: Upptäck StoryType-egenskapen för att enkelt identifiera och kategorisera dina berättelser, vilket förbättrar organiseringen och din berättarupplevelse.
type: docs
weight: 40
url: /sv/net/aspose.words/story/storytype/
---
## Story.StoryType property

Hämtar typen av den här berättelsen.

```csharp
public StoryType StoryType { get; }
```

## Exempel

Visar hur man tar bort alla former från en nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inbäddad form,
// som har ett förälderparagraf, som är en undernod till den första sektionens brödtext.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Vi kan ta bort alla former från underparagraferna i denna brödtext.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* enum [StoryType](../../storytype/)
* class [Story](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
