---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words pour .NET
description: Personnalisez votre design avec la propriété BackThemeColor. Définissez facilement un objet ThemeColor pour améliorer le remplissage de votre arrière-plan et améliorer l'expérience utilisateur.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage.

```csharp
public ThemeColor BackThemeColor { get; set; }
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
