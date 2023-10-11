---
title: AxisScaling.LogBase
second_title: Référence de l'API Aspose.Words pour .NET
description: AxisScaling propriété. Obtient ou définit la base logarithmique dun axe logarithmique.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Obtient ou définit la base logarithmique d'un axe logarithmique.

```csharp
public double LogBase { get; set; }
```

### Remarques

La propriété n'est pas prise en charge par les nouveaux graphiques MS Office 2016.

La plage valide d'une valeur à virgule flottante est supérieure ou égale à 2 et inférieure ou égale à 1 000. La propriété n'a d'effet que si[`Type`](../type/) est défini sur Logarithmic.

La définition de cette propriété définit le[`Type`](../type/) propriété àLogarithmic .

### Exemples

Montre comment appliquer une mise à l’échelle logarithmique à un axe de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Insère une série avec des coordonnées X/Y pour cinq points.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// La mise à l'échelle de l'axe X est linéaire par défaut,
// affichant des valeurs incrémentées uniformément qui couvrent notre plage de valeurs X (0, 1, 2, 3...).
// Un axe linéaire n'est pas idéal pour nos valeurs Y
// puisque les points avec les valeurs Y les plus petites seront plus difficiles à lire.
// Une échelle logarithmique en base 20 (1, 20, 400, 8000...)
// répartira les points tracés, nous permettant de lire plus facilement leurs valeurs sur le graphique.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Voir également

* class [AxisScaling](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../axisscaling/)
* Assemblée [Aspose.Words](../../../)


