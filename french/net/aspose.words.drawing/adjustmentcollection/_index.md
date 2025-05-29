---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.AdjustmentCollection : votre solution pour gérer les valeurs d'ajustement en lecture seule des formes. Améliorez la conception de vos documents sans effort !
type: docs
weight: 710
url: /fr/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Représente une collection en lecture seule de[`Adjustment`](../adjustment/) ajuster les valeurs appliquées à la forme spécifiée.

```csharp
public class AdjustmentCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Renvoie un ajustement à l'index spécifié. |

## Exemples

Montre comment travailler avec les valeurs brutes de réglage.

```csharp
Document doc = new Document(MyDir + "Rounded rectangle shape.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

AdjustmentCollection adjustments = shape.Adjustments;
Assert.AreEqual(1, adjustments.Count);

Adjustment adjustment = adjustments[0];
Assert.AreEqual("adj", adjustment.Name);
Assert.AreEqual(16667, adjustment.Value);

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
