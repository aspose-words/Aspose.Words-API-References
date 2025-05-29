---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartSeriesGroup-Eigenschaft „FirstSliceAngle“, um den ersten Segmentwinkel Ihres Kreisdiagramms in Grad anzupassen und so die Datenvisualisierung zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Ruft den Winkel des ersten Segments des übergeordneten Kreisdiagramms in Grad ab oder legt ihn fest.

```csharp
public int FirstSliceAngle { get; set; }
```

## Bemerkungen

Gilt für Seriengruppen derPie ,Pie3D undDoughnut Typen.

Der zulässige Wertebereich liegt zwischen 0 und 360 (einschließlich). Der Standardwert ist 0.

## Beispiele

Zeigt, wie man ein Ringdiagramm erstellt und formatiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Löschen Sie die standardmäßig generierte Serie.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Formatieren Sie das Ringdiagramm.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Siehe auch

* class [ChartSeriesGroup](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
