---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Adjustment, conçue pour améliorer vos formes avec des valeurs de réglage précises pour un formatage de document supérieur.
type: docs
weight: 700
url: /fr/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Représente les valeurs de réglage appliquées à la forme spécifiée.

```csharp
public class Adjustment
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Obtient le nom du réglage. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Obtient ou définit la valeur brute du réglage. |

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
