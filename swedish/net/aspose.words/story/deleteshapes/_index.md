---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words för .NET
description: Story DeleteShapes metod. Tar bort alla former från texten i denna berättelse i C#.
type: docs
weight: 70
url: /sv/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Tar bort alla former från texten i denna berättelse.

```csharp
public void DeleteShapes()
```

## Exempel

Visar hur man tar bort alla former från en nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inline-form,
// som har ett överordnat stycke, som är en underordnad nod till det första avsnittets Kropp.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Vi kan ta bort alla former från underordnade stycken i denna Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* class [Story](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
