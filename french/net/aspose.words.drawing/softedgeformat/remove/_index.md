---
title: SoftEdgeFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: Supprimez facilement SoftEdgeFormat de votre objet parent grâce à la méthode SoftEdgeFormat Remove. Simplifiez votre conception pour des résultats optimaux !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat.Remove method

Supprime[`SoftEdgeFormat`](../) de l'objet parent.

```csharp
public void Remove()
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

* class [SoftEdgeFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
