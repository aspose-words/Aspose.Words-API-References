---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Fill classe. Représente le formatage de remplissage pour un objet en C#.
type: docs
weight: 950
url: /fr/net/aspose.words.drawing/fill/
---
## Fill class

Représente le formatage de remplissage pour un objet.

Pour en savoir plus, visitez le[Travailler avec des éléments graphiques](https://docs.aspose.com/words/net/working-with-graphic-elements/) article documentaire.

```csharp
public class Fill
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Obtient ou définit un objet Color qui représente la couleur d'arrière-plan du remplissage. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Obtient ou définit un objet Color qui représente la couleur de premier plan du remplissage. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Obtient un type de remplissage. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Obtient ou définit un objet Color qui représente la couleur de premier plan du remplissage. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan du remplissage. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Obtient ou définit l'angle du remplissage dégradé. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Obtient une collection de[`GradientStop`](../gradientstop/) objets pour le remplissage. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Obtient le style de dégradé[`GradientStyle`](../gradientstyle/) pour le remplissage. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Obtient la variante de dégradé[`GradientVariant`](../gradientvariant/) pour le remplissage. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Obtient les octets bruts de la texture ou du motif de remplissage. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Obtient ou définit le degré d'opacité du remplissage spécifié sous la forme d'une valeur comprise entre 0,0 (clair) et 1,0 (opaque). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Obtient un[`PatternType`](../patterntype/) pour le remplissage. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Obtient un[`PresetTexture`](../presettexture/) pour le remplissage. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Obtient ou définit si le remplissage tourne avec l'objet spécifié. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Obtient ou définit l'alignement pour le remplissage de la texture des carreaux. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Obtient ou définit le degré de transparence du remplissage spécifié sous la forme d'une valeur comprise entre 0,0 (opaque) et 1,0 (clair). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Obtient ou définit la valeur qui est`vrai` si le formatage appliqué à cette instance, est visible. |

## Méthodes

| Nom | La description |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Définit le remplissage spécifié sur un dégradé d'une seule couleur. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Définit le remplissage spécifié sur un dégradé d'une seule couleur en utilisant la couleur spécifiée. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Définit le remplissage spécifié sur un motif. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Définit le remplissage spécifié sur un motif. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Définit le remplissage sur une texture prédéfinie. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Modifie le type de remplissage en image unique. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Modifie le type de remplissage en image unique. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Modifie le type de remplissage en image unique. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Définit le remplissage sur une couleur uniforme. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Définit le remplissage sur une couleur uniforme spécifiée. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Définit le remplissage spécifié sur un dégradé bicolore. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Définit le remplissage spécifié sur un dégradé bicolore. |

## Remarques

Utilisez le[`Fill`](../shapebase/fill/) ou[`Fill`](../../aspose.words/font/fill/) propriété pour accéder aux propriétés de remplissage d'un objet. Vous ne créez pas d'instances du`Fill` classe directement.

## Exemples

Montre comment remplir une forme avec une couleur unie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape.StrokeColor = Color.CadetBlue;

// Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape.FillColor = Color.LightBlue;

// La propriété "Opacité" détermine le degré de transparence de la couleur sur une échelle de 0 à 1,
// avec 1 étant entièrement opaque et 0 étant invisible.
// Le remplissage de la forme par défaut est entièrement opaque, nous ne pouvons donc pas voir le texte sur lequel se trouve cette forme.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Définit l'opacité de la couleur de remplissage de la forme sur une valeur inférieure afin que nous puissions voir le texte en dessous.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
