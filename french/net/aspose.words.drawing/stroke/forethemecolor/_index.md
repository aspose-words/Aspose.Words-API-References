---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words pour .NET
description: Gérez facilement la couleur de premier plan de votre trait grâce à la propriété Stroke ForeThemeColor. Personnalisez vos créations avec des couleurs de thème éclatantes !
type: docs
weight: 140
url: /fr/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan du trait.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
