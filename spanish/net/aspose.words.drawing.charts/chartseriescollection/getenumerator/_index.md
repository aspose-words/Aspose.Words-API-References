---
title: ChartSeriesCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Descubra el método GetEnumerator de ChartSeriesCollection: recupere de manera eficiente objetos enumeradores para lograr una manipulación y un análisis de datos sin inconvenientes.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartseriescollection/getenumerator/
---
## ChartSeriesCollection.GetEnumerator method

Devuelve un objeto enumerador.

```csharp
public IEnumerator<ChartSeries> GetEnumerator()
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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
