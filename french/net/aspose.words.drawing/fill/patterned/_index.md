---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Fill Patterned pour appliquer sans effort des motifs uniques à vos créations, améliorant ainsi la créativité et l'attrait visuel de vos projets.
type: docs
weight: 230
url: /fr/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Définit le remplissage spécifié sur un motif.

```csharp
public void Patterned(PatternType patternType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

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

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Définit le remplissage spécifié sur un motif.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | La couleur du remplissage du premier plan. |
| backColor | Color | La couleur du remplissage d'arrière-plan. |

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
