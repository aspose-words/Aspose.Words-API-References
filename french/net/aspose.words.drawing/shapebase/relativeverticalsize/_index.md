---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase RelativeVerticalSize pour ajuster facilement les dimensions verticales des formes pour une flexibilité et une précision de conception améliorées.
type: docs
weight: 480
url: /fr/net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

Obtient ou définit la valeur de la taille relative de la forme dans la direction verticale.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## Remarques

La valeur par défaut estMargin.

N'a d'effet que si[`HeightRelative`](../heightrelative/) est réglé.

## Exemples

Montre comment définir la taille et la position relatives.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajout d'une forme simple avec une taille et une position absolues.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Définissez WrapType sur WrapType.None car les formes en ligne sont automatiquement converties en unités absolues.
shape.WrapType = WrapType.None;

// Vérification et définition de la taille horizontale relative.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Définition de la taille horizontale de la liaison sur Marge.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Définition de la largeur à 50 % de la largeur de la marge.
    shape.WidthRelative = 50;
}

// Vérification et définition de la taille verticale relative.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Définition de la taille verticale de la liaison sur Marge.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Définition de la hauteur à 30 % de la hauteur de la marge.
    shape.HeightRelative = 30;
}

// Vérification et réglage de la position verticale relative.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // définir la position de liaison à TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Définition du Top relatif à 30 % de la position TopMargin.
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

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
