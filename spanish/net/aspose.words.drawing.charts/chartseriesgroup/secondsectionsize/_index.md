---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words para .NET
description: Descubra cómo ajustar la propiedad SecondSectionSize en ChartSeriesGroup para personalizar de manera efectiva el tamaño de la sección secundaria de su gráfico circular.
type: docs
weight: 90
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Obtiene o establece el tamaño de la sección secundaria del gráfico circular como un porcentaje.

```csharp
public int SecondSectionSize { get; set; }
```

## Observaciones

Se aplica a grupos de series de laPieOfPie y PieOfBar tipos.

El rango de valores aceptables va de 5 a 200 inclusive. El valor predeterminado es 75.

## Ejemplos

Muestra cómo crear y dar formato a un gráfico circular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
//Eliminar la serie generada por defecto.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Formatear el gráfico circular.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Ver también

* class [ChartSeriesGroup](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
