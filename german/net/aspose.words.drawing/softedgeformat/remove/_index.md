---
title: SoftEdgeFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entfernen Sie SoftEdgeFormat mühelos von Ihrem übergeordneten Objekt mit der Methode „SoftEdgeFormat Remove“. Optimieren Sie Ihr Design für optimale Ergebnisse!
type: docs
weight: 20
url: /de/net/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat.Remove method

Entfernt[`SoftEdgeFormat`](../) vom übergeordneten Objekt.

```csharp
public void Remove()
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
