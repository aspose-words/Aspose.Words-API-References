---
title: ChartSeriesCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeriesCollection Count, que proporciona el número total de ChartSeries en su colección para una mejor visualización de datos.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartseriescollection/count/
---
## ChartSeriesCollection.Count property

Devuelve el número de[`ChartSeries`](../../chartseries/) en esta colección.

```csharp
public int Count { get; }
```

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

* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
