---
title: Chart.DataTable
linktitle: DataTable
articleTitle: DataTable
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos auf die DataTable-Eigenschaften Ihres Diagramms zu und passen Sie sie an. Verbessern Sie die Datenvisualisierung mit der Eigenschaft „Anzeigen“ für klare Einblicke.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chart/datatable/
---
## Chart.DataTable property

Bietet Zugriff auf die Eigenschaften einer Datentabelle dieses Diagramms. Die Datentabelle kann angezeigt werden mit dem[`Show`](../../chartdatatable/show/) Eigenschaft.

```csharp
public ChartDataTable DataTable { get; }
```

## Beispiele

Zeigt, wie eine Datentabelle mit Diagrammreihendaten angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Siehe auch

* class [ChartDataTable](../../chartdatatable/)
* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
