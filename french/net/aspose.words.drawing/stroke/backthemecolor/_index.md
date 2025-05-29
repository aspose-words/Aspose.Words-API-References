---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words pour .NET
description: Personnalisez votre design avec la propriété Stroke BackThemeColor. Définissez facilement une couleur de thème pour l'arrière-plan de votre contour afin d'améliorer l'attrait visuel.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du trait.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
