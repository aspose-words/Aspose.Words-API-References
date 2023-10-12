---
title: Enum RelativeHorizontalSize
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.RelativeHorizontalSize énumération. Spécifie par rapport à quoi la largeur dune forme ou dun cadre de texte est calculée horizontalement.
type: docs
weight: 1200
url: /fr/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Spécifie par rapport à quoi la largeur d'une forme ou d'un cadre de texte est calculée horizontalement.

```csharp
public enum RelativeHorizontalSize
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Margin | `0` | Spécifie que la largeur est calculée par rapport à l'espace entre les marges gauche et droite. |
| Page | `1` | Spécifie que la largeur est calculée par rapport à la largeur de la page. |
| LeftMargin | `2` | Spécifie que la largeur est calculée par rapport à la taille de la zone de marge gauche. |
| RightMargin | `3` | Spécifie que la largeur est calculée par rapport à la taille de la zone de marge droite. |
| InnerMargin | `4` | Spécifie que la largeur est calculée par rapport à la taille de la zone de marge intérieure, à la taille de la zone de marge gauche pour les pages impaires et à la taille de la zone de marge droite pour les pages paires. |
| OuterMargin | `5` | Spécifie que la largeur est calculée par rapport à la taille de la zone de marge extérieure, à la taille de la zone de marge droite pour les pages impaires et à la taille de la zone de marge gauche pour les pages paires. |
| Default | `1` | La valeur par défaut estMargin . |

### Exemples

Montre comment définir la taille et la position relatives.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajout d'une forme simple avec une taille et une position absolues.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Définissez WrapType sur WrapType.None puisque les formes en ligne sont automatiquement converties en unités absolues.
shape.WrapType = WrapType.None;

// Vérification et définition de la taille horizontale relative.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Définition de la liaison de taille horizontale sur Marge.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Définition de la largeur à 50 % de la largeur de la marge.
    shape.WidthRelative = 50;
}

// Vérification et définition de la taille verticale relative.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Définition de la liaison de taille verticale sur Marge.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Définition de la hauteur à 30 % de la hauteur de la marge.
    shape.HeightRelative = 30;
}

// Vérification et réglage de la position verticale relative.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // définition de la liaison de position à TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Définition du Top relatif à 30 % de la position TopMargin.
    shape.TopRelative = 30;
}

// Vérification et réglage de la position horizontale relative.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Définition de la liaison de position sur RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // La valeur relative de la position peut être négative.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Voir également

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


