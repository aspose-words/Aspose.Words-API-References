---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Motif de remplissage pour accéder facilement au type de motif et le personnaliser pour vos créations. Sublimez vos projets avec des options de remplissage uniques !
type: docs
weight: 160
url: /fr/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Obtient un[`PatternType`](../../patterntype/) pour le remplissage.

```csharp
public PatternType Pattern { get; }
```

## Exemples

Montre comment définir un motif pour une forme.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Il existe plusieurs façons de spécifier le remplissage d'un motif.
// 1 - Appliquer le motif au remplissage de la forme :
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Appliquer un motif avec des couleurs de premier plan et d'arrière-plan au remplissage de la forme :
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Voir également

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
