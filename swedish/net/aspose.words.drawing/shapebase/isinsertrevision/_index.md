---
title: ShapeBase.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words för .NET
description: Upptäck hur ShapeBases IsInsertRevision-egenskap förbättrar dina Word-dokument genom att identifiera ändringar som gjorts under spårning. Öka din redigeringseffektivitet!
type: docs
weight: 320
url: /sv/net/aspose.words.drawing/shapebase/isinsertrevision/
---
## ShapeBase.IsInsertRevision property

Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsInsertRevision { get; }
```

## Exempel

Visar hur man arbetar med revisionsformer.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Infoga en inbäddad form utan att spåra revisioner, vilket gör att formen inte blir en revision av något slag.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Börja spåra revisioner och infoga sedan en annan form, som kommer att vara en revision.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Eftersom vi tog bort den formen medan vi spårade ändringar,
// formen finns kvar i dokumentet och räknas som en borttagningsrevision.
// Om du accepterar den här revisionen tas formen bort permanent, och om du avvisar den behålls den i dokumentet.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// Och vi infogade en annan form medan vi spårade ändringar, så den formen kommer att räknas som en infogningsrevidering.
// Att acceptera denna revision kommer att assimilera denna form i dokumentet som en icke-revision,
// och om du avvisar revisionen tas formen bort permanent.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
