---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.SoftEdgeFormat pour améliorer vos documents avec de superbes effets de bords doux pour un look professionnel.
type: docs
weight: 1710
url: /fr/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Représente la mise en forme des bords doux d'un objet.

```csharp
public class SoftEdgeFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Obtient ou définit une valeur double qui représente la longueur du rayon pour un effet de bord doux en points (pt). La valeur par défaut est 0,0. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Supprime`SoftEdgeFormat` de l'objet parent. |

## Remarques

Utilisez le[`SoftEdge`](../shapebase/softedge/) propriété pour accéder aux propriétés de bord souple d'un objet. Vous ne créez pas d'instances de la`SoftEdgeFormat` classe directement.

## Exemples

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

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
