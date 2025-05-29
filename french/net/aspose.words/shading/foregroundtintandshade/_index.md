---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words pour .NET
description: Ajustez la propriété ForegroundTintAndShade pour éclaircir ou assombrir sans effort les couleurs de votre thème, améliorant ainsi l'attrait visuel de votre conception.
type: docs
weight: 60
url: /fr/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancer si cette propriété est définie sur une valeur inférieure à -1 ou supérieure à 1. |
| InvalidOperationException | Lancer si cette propriété est définie pour l'objet Ombrage avec des couleurs non thématiques. |

## Remarques

Les valeurs autorisées sont comprises entre -1 (la plus foncée) et 1 (la plus claire) pour cette propriété.

Zéro (0) est neutre.

## Exemples

Montre comment définir les couleurs de premier plan et d'arrière-plan pour la texture d'ombrage.

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
