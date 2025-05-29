---
title: SoftEdgeFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words für .NET
description: Entdecken Sie die SoftEdgeFormat Radius-Eigenschaft, um weiche Kanteneffekte einfach anzupassen. Steuern Sie die Radiuslänge präzise für beeindruckende visuelle Ergebnisse.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/softedgeformat/radius/
---
## SoftEdgeFormat.Radius property

Ruft einen Double-Wert ab oder legt ihn fest, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0,0.

```csharp
public double Radius { get; set; }
```

## Beispiele

Zeigt, wie die Grenze für die Bildauflösung festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Zeigt, wie mit Soft-Edge-Formatierung gearbeitet wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Weiche Kante auf die Form anwenden.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Dokument mit rechteckiger Form und weicher Kante laden.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Überprüfen Sie den Radius der weichen Kante.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Weiche Kante aus der Form entfernen.
softEdgeFormat.Remove();

// Radius der entfernten weichen Kante prüfen.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Siehe auch

* class [SoftEdgeFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
