---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.SoftEdgeFormat, um Ihre Dokumente mit atemberaubenden Soft-Edge-Effekten für ein professionelles Aussehen zu verbessern.
type: docs
weight: 1710
url: /de/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Stellt die Soft-Edge-Formatierung für ein Objekt dar.

```csharp
public class SoftEdgeFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0,0. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Entfernt`SoftEdgeFormat` vom übergeordneten Objekt. |

## Bemerkungen

Verwenden Sie die[`SoftEdge`](../shapebase/softedge/) Eigenschaft, um auf die Soft-Edge-Eigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der`SoftEdgeFormat` Klasse direkt.

## Beispiele

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
