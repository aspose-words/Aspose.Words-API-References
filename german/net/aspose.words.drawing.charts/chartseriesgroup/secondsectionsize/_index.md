---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die SecondSectionSize-Eigenschaft in ChartSeriesGroup anpassen, um die Größe des sekundären Abschnitts Ihres Kreisdiagramms effektiv anzupassen.
type: docs
weight: 90
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Ruft die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz ab oder legt diese fest.

```csharp
public int SecondSectionSize { get; set; }
```

## Bemerkungen

Gilt für Seriengruppen derPieOfPie und PieOfBar Typen.

Der zulässige Wertebereich liegt zwischen 5 und 200 (einschließlich). Der Standardwert ist 75.

## Beispiele

Zeigt, wie man ein Kreisdiagramm erstellt und formatiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Löschen Sie die standardmäßig generierte Serie.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Formatieren Sie das Kreisdiagramm.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Siehe auch

* class [ChartSeriesGroup](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
