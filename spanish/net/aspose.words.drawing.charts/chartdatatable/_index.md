---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartDataTable para personalizar fácilmente las tablas de datos de gráficos y mejorar su visualización de datos con funciones potentes.
type: docs
weight: 990
url: /es/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Permite especificar propiedades de una tabla de datos de gráficos.

```csharp
public class ChartDataTable
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Proporciona acceso al formato de fuente de la tabla de datos. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Proporciona acceso para rellenar el fondo del texto y formatear el borde de la tabla de datos. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Obtiene o establece un indicador que indica si se muestra un borde horizontal de la tabla de datos. El valor predeterminado es`verdadero` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Obtiene o establece un indicador que indica si las claves de leyenda se muestran en la tabla de datos. El valor predeterminado es`verdadero` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Obtiene o establece un indicador que indica si se muestra un borde de contorno, es decir, un borde alrededor de los nombres de series y categorías. El valor predeterminado es`verdadero` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Obtiene o establece un indicador que indica si se muestra un borde vertical de la tabla de datos. El valor predeterminado es`verdadero` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Obtiene o establece un indicador que indica si la tabla de datos se mostrará para el gráfico. El valor predeterminado es`FALSO` . |

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
