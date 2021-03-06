---
title: Stroke
second_title: Référence de l'API Aspose.Words pour .NET
description: Définit un trait pour une forme.
type: docs
weight: 1160
url: /fr/net/aspose.words.drawing/stroke/
---
## Stroke class

Définit un trait pour une forme.

```csharp
public class Stroke
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor) { get; set; } | Obtient ou définit la couleur d'arrière-plan du trait. |
| [Color](../../aspose.words.drawing/stroke/color) { get; set; } | Définit la couleur d'un trait. |
| [Color2](../../aspose.words.drawing/stroke/color2) { get; set; } | Définit une deuxième couleur pour un trait. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle) { get; set; } | Spécifie le motif de points et de tirets pour un trait. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength) { get; set; } | Définit la longueur de la pointe de flèche pour la fin d'un trait. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype) { get; set; } | Définit la pointe de flèche pour la fin d'un trait. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth) { get; set; } | Définit la largeur de la pointe de flèche pour la fin d'un trait. |
| [EndCap](../../aspose.words.drawing/stroke/endcap) { get; set; } | Définit le style de capuchon pour la fin d'un trait. |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor) { get; set; } | Obtient ou définit la couleur de premier plan du trait. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes) { get; } | Définit l'image pour une image de contour ou un motif de remplissage. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle) { get; set; } | Définit le style de jointure d'une polyligne. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle) { get; set; } | Définit le style de trait du trait. |
| [On](../../aspose.words.drawing/stroke/on) { get; set; } | Définit si le chemin sera tracé. |
| [Opacity](../../aspose.words.drawing/stroke/opacity) { get; set; } | Définit la quantité de transparence d'un trait. La plage valide est de 0 à 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength) { get; set; } | Définit la longueur de la pointe de flèche pour le début d'un trait. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype) { get; set; } | Définit la pointe de flèche pour le début d'un trait. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth) { get; set; } | Définit la largeur de la pointe de flèche pour le début d'un trait. |
| [Transparency](../../aspose.words.drawing/stroke/transparency) { get; set; } | Obtient ou définit une valeur comprise entre 0,0 (opaque) et 1,0 (clair) représentant le degré de transparence du trait. |
| [Visible](../../aspose.words.drawing/stroke/visible) { get; set; } | Obtient ou définit un indicateur indiquant si le trait est visible. |
| [Weight](../../aspose.words.drawing/stroke/weight) { get; set; } | Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points. |

### Remarques

Utilisez le[`Stroke`](../shape/stroke)pour accéder aux propriétés de trait d'une forme. Vous ne créez pas d'instances de la[`Stroke`](../stroke) classe directement.

### Exemples

Montre comment modifier les propriétés de trait.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Les formes de base, telles que le rectangle, ont deux parties visibles.
// 1 - Le remplissage, qui s'applique à la zone à l'intérieur du contour de la forme :
shape.Fill.ForeColor = Color.White;

// 2 - Le trait, qui marque le contour de la forme :
// Modifie diverses propriétés du trait de cette forme.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
