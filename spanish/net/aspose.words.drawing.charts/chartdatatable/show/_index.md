---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words para .NET
description: Controle la visibilidad de su gráfico con la propiedad ChartDataTable Show. Active y desactive fácilmente la visualización de la tabla de datos para obtener información más detallada. El valor predeterminado es falso.
type: docs
weight: 70
url: /es/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

Obtiene o establece un indicador que indica si la tabla de datos se mostrará para el gráfico. El valor predeterminado es`FALSO` .

```csharp
public bool Show { get; set; }
```

## Observaciones

Los siguientes tipos de gráficos no admiten tablas de datos: Dispersión, Circular, Anillo, Superficie, Radar, Mapa de árbol, Rayo de sol, Histograma, Pareto, Caja y bigotes, Cascada, Embudo y gráficos combinados que incluyen series de estos tipos. Mostrar una tabla de datos para estos tipos de gráficos genera un error.InvalidOperationException excepción.

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

* class [ChartDataTable](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
