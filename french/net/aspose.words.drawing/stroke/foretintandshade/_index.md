---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words pour .NET
description: Ajustez la propriété Stroke ForeTintAndShade pour éclaircir ou assombrir sans effort la couleur de premier plan de votre trait pour un impact visuel amélioré.
type: docs
weight: 150
url: /fr/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait.

```csharp
public double ForeTintAndShade { get; set; }
```

## Remarques

Les valeurs autorisées pour cette propriété sont comprises entre -1 (la plus foncée) et 1 (la plus claire). Zéro (0) est neutre. Toute tentative de définition de cette propriété sur une valeur inférieure à -1 ou supérieure à 1 entraîne l'erreur suivante :ArgumentOutOfRangeException.

## Exemples

Montre comment définir la couleur, la teinte et l'ombre du thème principal.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Voir également

* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
