---
title: Class Stroke
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Stroke classe. Définit un trait pour une forme.
type: docs
weight: 1310
url: /fr/net/aspose.words.drawing/stroke/
---
## Stroke class

Définit un trait pour une forme.

Pour en savoir plus, visitez le[Travailler avec des formes](https://docs.aspose.com/words/net/working-with-shapes/) article documentaire.

```csharp
public class Stroke
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Obtient ou définit la couleur d'arrière-plan du trait. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } |  |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Définit la couleur d'un trait. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Définit une deuxième couleur pour un trait. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Spécifie le motif de points et de tirets pour un trait. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Définit la longueur de la pointe de flèche pour la fin d'un trait. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Définit la pointe de flèche pour la fin d'un trait. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Définit la largeur de la pointe de flèche pour la fin d'un trait. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Définit le style de capuchon pour la fin d'un trait. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Obtient le formatage de remplissage pour le`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Obtient ou définit la couleur de premier plan du trait. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Définit l'image pour une image de trait ou un remplissage de motif. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Définit le style de jointure d'une polyligne. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Définit le style de ligne du trait. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Définit si le chemin sera tracé. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Définit la quantité de transparence d'un trait. La plage valide est de 0 à 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Définit la longueur de la pointe de flèche pour le début d'un trait. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Définit la pointe de flèche pour le début d'un trait. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Définit la largeur de la pointe de flèche pour le début d'un trait. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Obtient ou définit une valeur comprise entre 0,0 (opaque) et 1,0 (clair) représentant le degré de transparence du trait. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Obtient ou définit un indicateur indiquant si le trait est visible. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points. |

### Remarques

Utilisez le[`Stroke`](../shape/stroke/) propriété pour accéder aux propriétés de trait d'une forme. Vous ne créez pas d'instances du`Stroke` classe directement.

### Exemples

Montre comment modifier les propriétés du trait.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Les formes de base, comme le rectangle, comportent deux parties visibles.
// 1 - Le remplissage, qui s'applique à la zone située à l'intérieur du contour de la forme :
shape.Fill.ForeColor = Color.White;

// 2 - Le trait, qui marque le contour de la forme :
// Modifier diverses propriétés du trait de cette forme.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


