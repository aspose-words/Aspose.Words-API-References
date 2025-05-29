---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words pour .NET
description: Découvrez les ajustements de forme. Accédez aux valeurs brutes pour des modifications de forme précises. Améliorez facilement vos créations grâce à des ajustements sur mesure pour des résultats optimaux.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Donne accès aux valeurs brutes de réglage d'une forme. Pour une forme qui ne contient aucune valeur brute de réglage, elle renvoie une collection vide.

```csharp
public AdjustmentCollection Adjustments { get; }
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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
