---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Item AdjustmentCollection, récupérez sans effort les ajustements par index pour une gestion transparente des données et des performances améliorées.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Renvoie un ajustement à l'index spécifié.

```csharp
public Adjustment this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index de la collection. |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
