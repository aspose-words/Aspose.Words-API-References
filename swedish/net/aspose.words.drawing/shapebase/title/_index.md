---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words för .NET
description: Hantera din ShapeBase-titelegenskap utan ansträngning. Ställ in eller hämta titelbilden för valfritt formobjekt för att förbättra din designs tydlighet och attraktionskraft.
type: docs
weight: 570
url: /sv/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Hämtar eller anger titeln (bildtexten) för det aktuella formobjektet.

```csharp
public string Title { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Kan inte vara`null`, men kan vara en tom sträng.

## Exempel

Visar hur man ställer in titeln på en form.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en form, ge den en titel och lägg sedan till den i dokumentet.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// När vi sparar ett dokument med en form som har en titel,
// Aspose.Words kommer att lagra den titeln i formens Alt-text.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
