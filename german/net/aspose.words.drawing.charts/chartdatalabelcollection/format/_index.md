---
title: ChartDataLabelCollection.Format
second_title: Aspose.Words für .NET-API-Referenz
description: ChartDataLabelCollection eigendom. Bietet Zugriff auf die Füll und Zeilenformatierung der Datenbeschriftungen.
type: docs
weight: 30
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Bietet Zugriff auf die Füll- und Zeilenformatierung der Datenbeschriftungen.

```csharp
public ChartFormat Format { get; }
```

### Beispiele

Zeigt, wie Füll-, Strich- und Beschriftungsformatierungen für Diagrammdatenbeschriftungen festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Neue Serie hinzufügen.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Datenbeschriftungen als Callouts formatieren.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Füllung und Strich einer einzelnen Datenbeschriftung ändern.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Siehe auch

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* Montage [Aspose.Words](../../../)


