---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words pour .NET
description: Découvrez comment définir la propriété ForeThemeColor pour personnaliser votre design avec des couleurs de remplissage éclatantes. Améliorez l'attrait visuel de votre projet sans effort !
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan pour le remplissage.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
