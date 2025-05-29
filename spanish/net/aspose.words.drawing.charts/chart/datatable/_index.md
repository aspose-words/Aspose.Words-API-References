---
title: Chart.DataTable
linktitle: DataTable
articleTitle: DataTable
second_title: Aspose.Words para .NET
description: Acceda y personalice fácilmente las propiedades de DataTable de su gráfico. Mejore la visualización de datos con la propiedad Mostrar para obtener información clara.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chart/datatable/
---
## Chart.DataTable property

Proporciona acceso a las propiedades de una tabla de datos de este gráfico. La tabla de datos se puede mostrar utilizando el[`Show`](../../chartdatatable/show/) propiedad.

```csharp
public ChartDataTable DataTable { get; }
```

## Ejemplos

Muestra cómo mostrar una tabla de datos con datos de series de gráficos.

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

### Ver también

* class [ChartDataTable](../../chartdatatable/)
* class [Chart](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
