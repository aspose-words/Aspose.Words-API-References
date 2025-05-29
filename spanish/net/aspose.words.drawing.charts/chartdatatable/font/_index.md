---
title: ChartDataTable.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: Descubra la propiedad Fuente ChartDataTable para mejorar la apariencia de su tabla de datos con formato de fuente personalizable para una mejor legibilidad e impacto.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartdatatable/font/
---
## ChartDataTable.Font property

Proporciona acceso al formato de fuente de la tabla de datos.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartDataTable](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
