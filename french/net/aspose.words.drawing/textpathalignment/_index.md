---
title: TextPathAlignment Enum
linktitle: TextPathAlignment
articleTitle: TextPathAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.TextPathAlignment pour un alignement précis de vos WordArts. Améliorez la conception de vos documents grâce à des options de texte polyvalentes !
type: docs
weight: 1770
url: /fr/net/aspose.words.drawing/textpathalignment/
---
## TextPathAlignment enumeration

Alignement WordArt.

```csharp
public enum TextPathAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Stretch | `0` | Étirez chaque ligne de texte pour l'adapter à la largeur. |
| Center | `1` | Centrer le texte sur la largeur. |
| Left | `2` | Justifier à gauche. |
| Right | `3` | Justifier à droite. |
| LetterJustify | `4` | Étalez les lettres pour qu'elles s'adaptent à la largeur. |
| WordJustify | `5` | Répartissez les mots pour qu'ils s'adaptent à la largeur. |

## Exemples

Montre comment travailler avec WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Insérez un objet WordArt pour afficher du texte dans une forme que nous pouvons redimensionner et déplacer à l'aide de la souris dans Microsoft Word.
    // Fournissez un « ShapeType » comme argument pour définir une forme pour le WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Appliquez les paramètres de formatage « Gras » et « Italique » au texte à l'aide des propriétés respectives.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Vous trouverez ci-dessous diverses autres propriétés liées au formatage du texte.
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    // Utilisez la propriété « On » pour afficher/masquer le texte.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Utilisez la propriété « Kerning » pour activer/désactiver l'espacement de crénage entre certains caractères.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Utilisez la propriété « Espacement » pour définir l'espacement personnalisé entre les caractères sur une échelle de 0,0 (aucun) à 1,0 (par défaut).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Définissez la propriété « RotateLetters » sur « true » pour faire pivoter chaque caractère de 90 degrés dans le sens inverse des aiguilles d'une montre.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Définissez la propriété « SameLetterHeights » sur « true » pour que la hauteur x de chaque caractère soit égale à la hauteur des majuscules.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Par défaut, la taille du texte sera toujours mise à l'échelle pour s'adapter à la taille de la forme contenante, remplaçant le paramètre de taille du texte.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Si nous définissons la propriété "FitShape: sur "false", le texte conservera la taille
    // que la propriété « Taille » spécifie quelle que soit la taille de la forme.
    // Utilisez également la propriété « TextPathAlignment » pour aligner le texte sur un côté de la forme.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Insérer un nouveau paragraphe avec une forme WordArt à l'intérieur.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Créez une forme en ligne, qui servira de conteneur pour notre WordArt.
    // La forme ne peut être une forme WordArt valide que si nous lui attribuons un ShapeType désigné par WordArt.
    // Ces types auront « objet WordArt » dans la description,
    // et leurs noms de constantes d'énumération commenceront tous par « Texte ».
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### Voir également

* property [TextPathAlignment](../textpath/textpathalignment/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
