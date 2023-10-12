---
title: Shading.ForegroundPatternThemeColor
second_title: Référence de l'API Aspose.Words pour .NET
description: Shading propriété. Obtient ou définit la couleur du thème du motif de premier plan dans le jeu de couleurs appliqué associé à ceShading objet.
type: docs
weight: 50
url: /fr/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

Obtient ou définit la couleur du thème du motif de premier plan dans le jeu de couleurs appliqué associé à ce[`Shading`](../) objet.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

### Exemples

Montre comment définir les couleurs de premier plan et d’arrière-plan pour l’ombrage de la texture.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Voir également

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* espace de noms [Aspose.Words](../../shading/)
* Assemblée [Aspose.Words](../../../)


