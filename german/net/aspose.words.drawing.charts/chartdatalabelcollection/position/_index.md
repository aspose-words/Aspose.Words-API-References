---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words für .NET
description: Entdecken Sie die Positionseigenschaft der ChartDataLabelCollection, um die Positionen Ihrer Datenbeschriftungen für eine verbesserte Datenvisualisierung und Übersichtlichkeit einfach anzupassen.
type: docs
weight: 70
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

Ruft die Position der Datenbeschriftungen ab oder legt sie fest.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Bemerkungen

Die Position kann für Datenbeschriftungen der folgenden Diagrammreihentypen festgelegt werden:

-Bar ,Column , Histogram ,Pareto , Waterfall ; zulässige Werte:Center , InsideBase ,InsideEnd und OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; allowed Werte:Center ,InsideBase undInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock ; zulässige Werte:Center , Left ,Right , Above UndBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie ; zulässige Werte: Center ,InsideEnd , OutsideEnd UndBestFit;

-BoxAndWhisker ; zulässige Werte: Left ,Right , Above UndBelow.

## Beispiele

Zeigt, wie die Position der Datenbeschriftung festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Säulendiagramm einfügen.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

// Serie hinzufügen.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Datenbeschriftungen anzeigen und Schriftfarbe festlegen.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Position der Datenbeschriftung festlegen.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Siehe auch

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
