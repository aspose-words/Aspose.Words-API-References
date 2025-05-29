---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words pour .NET
description: Ajustez la propriété BackTintAndShade pour éclaircir ou assombrir sans effort votre couleur d'arrière-plan, améliorant ainsi l'attrait visuel et l'expérience utilisateur de votre conception.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan.

```csharp
public double BackTintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancer si cette propriété est définie sur une valeur inférieure à -1 ou supérieure à 1. |

## Remarques

Les valeurs autorisées sont comprises entre -1 (la plus foncée) et 1 (la plus claire) pour cette propriété.

Zéro (0) est neutre.

## Exemples

Montre comment définir la couleur du thème pour la couleur de la forme de premier plan/arrière-plan.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Remarque : n'utilisez pas « BackThemeColor » et « BackTintAndShade » pour le remplissage de la police.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
