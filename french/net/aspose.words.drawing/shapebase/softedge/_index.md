---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words pour .NET
description: Sublimez vos créations avec ShapeBase SoftEdge pour une mise en forme fluide et des bords adoucis. Sublimez vos visuels sans effort et démarquez-vous dans chaque projet !
type: docs
weight: 550
url: /fr/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

Obtient une mise en forme des bords doux pour la forme.

```csharp
public SoftEdgeFormat SoftEdge { get; }
```

## Exemples

Montre comment définir une limite pour la résolution de l'image.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Montre comment travailler avec la mise en forme des bords doux.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Appliquer un bord doux à la forme.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Charger un document avec une forme rectangulaire avec un bord doux.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Vérifiez le rayon du bord souple.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Supprimez le bord doux de la forme.
softEdgeFormat.Remove();

// Vérifiez le rayon du bord souple supprimé.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Voir également

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
