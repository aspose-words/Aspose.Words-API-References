---
title: ChartDataTable.HasLegendKeys
linktitle: HasLegendKeys
articleTitle: HasLegendKeys
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartDataTable HasLegendKeys para controlar fácilmente la visibilidad de las claves de leyenda en su tabla de datos. ¡Mejore la claridad con configuraciones personalizables!
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/chartdatatable/haslegendkeys/
---
## ChartDataTable.HasLegendKeys property

Obtiene o establece un indicador que indica si las claves de leyenda se muestran en la tabla de datos. El valor predeterminado es`verdadero` .

```csharp
public bool HasLegendKeys { get; set; }
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

* class [ChartDataTable](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
