---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die DoughnutHoleSize-Eigenschaft von ChartSeriesGroup, um die Lochgröße Ihres Ringdiagramms in Prozent für eine verbesserte Datenvisualisierung einfach anzupassen.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Ruft die Lochgröße des übergeordneten Ringdiagramms als Prozentsatz ab oder legt sie fest.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Bemerkungen

Gilt nur für Seriengruppen derDoughnut Typ.

Der zulässige Wertebereich liegt zwischen 0 und 90 (einschließlich). Der Standardwert ist 75.

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
