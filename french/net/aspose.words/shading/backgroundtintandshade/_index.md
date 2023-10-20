---
title: Shading.BackgroundTintAndShade
linktitle: BackgroundTintAndShade
articleTitle: BackgroundTintAndShade
second_title: Aspose.Words pour .NET
description: Shading BackgroundTintAndShade propriété. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur dun thème darrièreplan en C#.
type: docs
weight: 30
url: /fr/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'un thème d'arrière-plan.

```csharp
public double BackgroundTintAndShade { get; set; }
```

## Remarques

Les valeurs autorisées sont comprises entre -1 (le plus sombre) et 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété sur une valeur inférieure à -1 ou supérieure à 1 entraîneArgumentOutOfRangeException.

La définition de cette propriété pour l'objet Shading avec des couleurs non thématiques entraîneInvalidOperationException.

## Exemples

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

* class [Shading](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
