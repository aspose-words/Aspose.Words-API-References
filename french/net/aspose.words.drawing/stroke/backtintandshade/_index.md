---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words pour .NET
description: Ajustez facilement la couleur d'arrière-plan de votre trait avec Stroke BackTintAndShade. Contrôlez la luminosité et l'obscurité pour un résultat parfait.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait.

```csharp
public double BackTintAndShade { get; set; }
```

## Remarques

Les valeurs autorisées pour cette propriété sont comprises entre -1 (la plus foncée) et 1 (la plus claire). Zéro (0) est neutre. Toute tentative de définition de cette propriété sur une valeur inférieure à -1 ou supérieure à 1 entraîne l'erreur suivante :ArgumentOutOfRangeException.

## Exemples

Montre comment définir la couleur, la teinte et l'ombre du thème.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Voir également

* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
