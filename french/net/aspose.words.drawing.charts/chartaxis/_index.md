---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartAxis classe. Représente les options daxe du graphique en C#.
type: docs
weight: 630
url: /fr/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Représente les options d'axe du graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartAxis
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Obtient ou définit un indicateur indiquant si l'axe des valeurs croise l'axe des catégories entre les catégories. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Renvoie ou définit la plus petite unité de temps représentée sur l'axe des catégories de temps. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Obtient ou définit le type de l'axe des catégories. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Spécifie comment cet axe croise l'axe perpendiculaire. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Spécifie l'endroit où l'axe se croise sur l'axe perpendiculaire. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Spécifie la valeur de mise à l'échelle des unités d'affichage pour l'axe des valeurs. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Renvoie le document auquel appartient le titulaire du titre. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Obtient ou définit un indicateur indiquant si l'axe a un quadrillage principal. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Obtient ou définit un indicateur indiquant si l'axe a un quadrillage mineur. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Obtient ou définit un indicateur indiquant si cet axe est masqué ou non. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Renvoie ou définit les principales graduations. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Renvoie ou définit la distance entre les graduations principales. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Obtient ou définit un indicateur indiquant si la distance par défaut entre les principales graduations doit être utilisée. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Renvoie ou définit la valeur d'échelle pour les graduations principales sur l'axe des catégories de temps. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Renvoie ou définit les graduations mineures pour l'axe. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Renvoie ou définit la distance entre les graduations mineures. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Obtient ou définit un indicateur indiquant si la distance par défaut entre les graduations mineures doit être utilisée. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Renvoie ou définit la valeur d'échelle pour les graduations mineures sur l'axe des catégories de temps. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Renvoie un[`ChartNumberFormat`](../chartnumberformat/) objet qui permet de définir des formats numériques pour l'axe. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Renvoie ou définit un indicateur indiquant si les valeurs de l'axe doivent être affichées dans l'ordre inverse, c'est-à-dire de max à min. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Donne accès aux options de mise à l'échelle de l'axe. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Obtient ou définit l'alignement du texte des étiquettes de graduation d'axe. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Obtient ou définit la distance des étiquettes par rapport à l'axe. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Renvoie ou définit la position des étiquettes de graduation sur l'axe. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Obtient ou définit l'intervalle auquel les étiquettes de graduation sont dessinées. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Obtient ou définit un indicateur indiquant si l'intervalle automatique de dessin des étiquettes de graduation doit être utilisé. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Obtient ou définit l'intervalle auquel les graduations sont dessinées. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Donne accès aux propriétés du titre de l'axe. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Renvoie le type de l'axe. |

## Exemples

Montre comment insérer un graphique et modifier l’apparence de ses axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Insère une série de graphiques avec des catégories pour l'axe X et des valeurs numériques respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Les axes du graphique ont diverses options permettant de modifier leur apparence,
// tels que leur direction, les graduations des unités majeures/mineures et les graduations.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Les graphiques à colonnes n'ont pas d'axe Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
