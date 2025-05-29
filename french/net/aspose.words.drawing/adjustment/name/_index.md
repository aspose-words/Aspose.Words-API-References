---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Nom de l'ajustement pour accéder et gérer facilement vos ajustements pour une efficacité améliorée et des flux de travail rationalisés.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Obtient le nom du réglage.

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
