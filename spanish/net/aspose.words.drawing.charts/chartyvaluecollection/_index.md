---
title: Class ChartYValueCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartYValueCollection clase. Representa una colección de valores Y para una serie de gráficos.
type: docs
weight: 880
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
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Obtiene el número de elementos de esta colección. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Obtiene o establece el valor Y en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Devuelve un objeto enumerador. |

### Observaciones

Todos los artículos de la colección excepto **nulo** debe tener el mismo[`ValueType`](../chartyvalue/valuetype/).

La colección solo permite cambiar los valores de Y. Para agregar o insertar nuevos valores a una serie de gráficos, o eliminar valores, los métodos apropiados del[`ChartSeries`](../chartseries/) Se puede utilizar la clase.

### Ejemplos

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
    // Borrar formato individual de todos los puntos de datos.
    // Los puntos de datos y los valores de datos son uno a uno en los gráficos de columnas.
    series.DataPoints[i].ClearFormat();

    // Obtener el valor Y.
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


