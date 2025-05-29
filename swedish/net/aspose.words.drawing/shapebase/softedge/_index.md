---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words för .NET
description: Förbättra dina designer med ShapeBase SoftEdge för mjuk och smidig formatering. Förhöj dina visuella element utan ansträngning och stick ut i varje projekt!
type: docs
weight: 550
url: /sv/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

Hämtar mjuka kanter för formen.

```csharp
public SoftEdgeFormat SoftEdge { get; }
```

## Exempel

Visar hur man ställer in en gräns för bildupplösning.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Visar hur man arbetar med mjuka kanter.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Applicera en mjuk kant på formen.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Ladda dokument med rektangulär form med mjuk kant.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Kontrollera mjukkantens radie.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Ta bort den mjuka kanten från formen.
softEdgeFormat.Remove();

// Kontrollera radien på den borttagna mjuka kanten.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Se även

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
