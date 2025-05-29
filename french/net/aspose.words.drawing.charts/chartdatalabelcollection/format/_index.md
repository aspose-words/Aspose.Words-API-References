---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Format ChartDataLabelCollection pour accéder facilement à des formats de remplissage et de ligne personnalisables pour vos étiquettes de données. Améliorez vos graphiques dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Donne accès au remplissage et au formatage des lignes des étiquettes de données.

```csharp
public ChartFormat Format { get; }
```

## Exemples

Montre comment définir le formatage du remplissage, du contour et des légendes pour les étiquettes de données du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une nouvelle série.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formater les étiquettes de données sous forme d'appels.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Modifier le remplissage et le contour d'une étiquette de données individuelle.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Voir également

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
