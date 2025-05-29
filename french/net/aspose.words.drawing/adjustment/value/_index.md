---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Valeur d'ajustement, obtenez ou définissez facilement des valeurs d'ajustement brutes pour améliorer la gestion de vos données et rationaliser vos processus.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Obtient ou définit la valeur brute du réglage.

```csharp
public int Value { get; set; }
```

## Remarques

Une valeur d'ajustement est simplement un guide qui a une formule basée sur une valeur spécifiée. Autrement dit, aucun calcul n'a lieu pour un guide de valeur d'ajustement. Au lieu de cela, ce guide spécifie une valeur de paramètre qui est utilisée pour les calculs dans les guides de forme.

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

* class [Adjustment](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
