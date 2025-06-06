---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartSeriesCollection, su solución para administrar y personalizar series de gráficos sin esfuerzo.
type: docs
weight: 1080
url: /es/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Representa una colección de un[`ChartSeries`](../chartseries/) .

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Devuelve el número de[`ChartSeries`](../chartseries/) en esta colección. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Devuelve un[`ChartSeries`](../chartseries/) en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) a esta colección. Utilice este método para agregar series a los gráficos de histograma. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, ChartMultilevelValue[], double[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) esta colección. Utilice este método para agregar series que tengan categorías de datos de varios niveles. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_4)(*string, DateTime[], double[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráficos de área, radar y acciones. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, double[], double[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráfico de dispersión. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_5)(*string, string[], double[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráficos de barras, columnas, líneas y superficies. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, double[], double[], double[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráfico de burbujas. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_6)(*string, string[], double[], bool[]*) | Agrega nuevo[`ChartSeries`](../chartseries/) a esta colección. Utilice este método para agregar series a los gráficos de cascada. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Elimina todo[`ChartSeries`](../chartseries/) de esta colección. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Elimina un[`ChartSeries`](../chartseries/) en el índice especificado. |

## Ejemplos

Muestra cómo agregar y eliminar datos de series en un gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un gráfico de columnas que contendrá tres series de datos de demostración de forma predeterminada.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

//Cada serie tiene cuatro valores decimales: uno para cada una de las cuatro categorías.
// Cuatro grupos de tres columnas representarán estos datos.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Imprime el nombre de cada serie en el gráfico.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

//Estos son los nombres de las categorías en el gráfico.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

//Podemos agregar una serie con nuevos valores para categorías existentes.
//Este gráfico ahora contendrá cuatro grupos de cuatro columnas.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
//Una serie de gráficos también se puede eliminar por índice, de esta manera.
// Esto eliminará una de las tres series de demostración que venían con el gráfico.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// También podemos borrar todos los datos del gráfico a la vez con este método.
// Al crear un nuevo gráfico, esta es la forma de borrar todos los datos de demostración
//antes de que podamos empezar a trabajar en un gráfico en blanco.
chartData.Clear();
```

### Ver también

* class [ChartSeries](../chartseries/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
