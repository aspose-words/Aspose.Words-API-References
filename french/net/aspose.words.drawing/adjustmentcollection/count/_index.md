---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété AdjustmentCollection Count pour récupérer facilement le nombre total d'éléments, améliorant ainsi l'efficacité de votre gestion des données.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Obtient le nombre d'éléments contenus dans la collection.

```csharp
public int Count { get; }
```

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

* class [AdjustmentCollection](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
