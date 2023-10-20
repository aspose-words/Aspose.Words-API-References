---
title: AxisBound.ValueAsDate
linktitle: ValueAsDate
articleTitle: ValueAsDate
second_title: Aspose.Words pour .NET
description: AxisBound ValueAsDate propriété. Renvoie la valeur de la limite de laxe représentée par datetime en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/axisbound/valueasdate/
---
## AxisBound.ValueAsDate property

Renvoie la valeur de la limite de l'axe représentée par datetime.

```csharp
public DateTime ValueAsDate { get; }
```

## Exemples

Montre comment définir les limites des axes personnalisés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Ajoute une série avec deux tableaux décimaux. Le premier tableau contient les valeurs X,
// et le second contient les valeurs Y correspondantes pour les points du nuage de points.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Par défaut, la mise à l'échelle par défaut est appliquée aux axes X et Y du graphique,
// afin que leurs deux plages soient suffisamment grandes pour englober toutes les valeurs X et Y de chaque série.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Nous pouvons définir nos propres limites d'axe.
// Dans ce cas, nous ferons en sorte que les règles des axes X et Y affichent une plage de 0 à 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Créez un graphique linéaire avec une série nécessitant une plage de dates sur l'axe X et des valeurs décimales pour l'axe Y.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// Nous pouvons également définir les limites des axes sous forme de dates, limitant le graphique à une période.
// Définir la plage sur 1980-1990 omettra les deux valeurs de la série
// qui sont en dehors de la plage du graphique.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Voir également

* class [AxisBound](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
