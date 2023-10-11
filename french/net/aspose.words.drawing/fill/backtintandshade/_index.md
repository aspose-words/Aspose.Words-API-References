---
title: Fill.BackTintAndShade
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill propriété. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur darrièreplan.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan.

```csharp
public double BackTintAndShade { get; set; }
```

### Remarques

Les valeurs autorisées sont comprises entre -1 (le plus sombre) et 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété sur une valeur inférieure à -1 ou supérieure à 1 entraîneArgumentOutOfRangeException.

### Exemples

Montre comment définir la couleur du thème pour la couleur de la forme de premier plan/arrière-plan.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Remarque : n'utilisez pas "BackThemeColor" et "BackTintAndShade" pour le remplissage de la police.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


