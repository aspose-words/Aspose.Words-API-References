---
title: ChartFormat.ShapeType
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartFormat propriété. Obtient ou définit le type de forme de lélément de graphique parent.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Obtient ou définit le type de forme de l'élément de graphique parent.

```csharp
public ChartShapeType ShapeType { get; set; }
```

### Remarques

Actuellement, la propriété ne peut être utilisée que pour les étiquettes de données.

### Exemples

Montre comment définir le formatage du remplissage, du contour et des légendes pour les étiquettes de données de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Supprime la série générée par défaut.
chart.Series.Clear();

// Ajouter une nouvelle série.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formate les étiquettes de données sous forme de légendes.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Modifie le remplissage et le contour d'une étiquette de données individuelle.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Voir également

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartformat/)
* Assemblée [Aspose.Words](../../../)


