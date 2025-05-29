---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
articleTitle: ChartXValueCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartXValueCollection, su solución para administrar colecciones de valores X en series de gráficos de manera efectiva.
type: docs
weight: 1170
url: /es/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Representa una colección de valores X para una serie de gráficos.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Obtiene el número de elementos en esta colección. |
| [FormatCode](../../aspose.words.drawing.charts/chartxvaluecollection/formatcode/) { get; set; } | Obtiene o establece el código de formato aplicado a los valores X. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Obtiene o establece el valor X en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Devuelve un objeto enumerador. |

## Observaciones

Todos los artículos de la colección excepto**nulo** debe tener el mismo[`ValueType`](../chartxvalue/valuetype/).

La colección solo permite cambiar los valores X. Para agregar o insertar nuevos valores a una serie de gráficos, o eliminar valores, utilice los métodos apropiados de la[`ChartSeries`](../chartseries/) La clase se puede utilizar.

## Ejemplos

Muestra cómo obtener datos de series de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Borrar el formato individual de todos los puntos de datos.
    // Los puntos de datos y los valores de los datos son uno a uno en los gráficos de columnas.
    series.DataPoints[i].ClearFormat();

    // Obtener el valor de Y.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Cambia los colores de los valores máximo y mínimo.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Ver también

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
