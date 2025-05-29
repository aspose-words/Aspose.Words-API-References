---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartYValueCollection, su solución ideal para administrar valores Y en series de gráficos de manera eficiente y eficaz.
type: docs
weight: 1200
url: /es/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

Representa una colección de valores Y para una serie de gráficos.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Obtiene el número de elementos en esta colección. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | Obtiene o establece el código de formato aplicado a los valores Y. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Obtiene o establece el valor Y en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Devuelve un objeto enumerador. |

## Observaciones

Todos los artículos de la colección excepto**nulo** debe tener el mismo[`ValueType`](../chartyvalue/valuetype/).

La colección solo permite cambiar los valores Y. Para agregar o insertar nuevos valores a una serie de gráficos, o eliminar valores, utilice los métodos apropiados de la[`ChartSeries`](../chartseries/) La clase se puede utilizar.

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
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
