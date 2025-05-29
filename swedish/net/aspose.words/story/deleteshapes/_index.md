---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words för .NET
description: Ta enkelt bort alla former från din berättelsetext med metoden DeleteShapes. Förenkla ditt innehåll och öka tydligheten idag!
type: docs
weight: 70
url: /sv/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Tar bort alla former från texten i den här berättelsen.

```csharp
public void DeleteShapes()
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

* class [Story](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
