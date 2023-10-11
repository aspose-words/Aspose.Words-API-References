---
title: Fill.BackThemeColor
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill propriété. Obtient ou définit un objet ThemeColor qui représente la couleur darrièreplan du remplissage.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


