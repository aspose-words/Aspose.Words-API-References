---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartSeriesCollection, din lösning för att enkelt hantera och anpassa diagramserier.
type: docs
weight: 1080
url: /sv/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Representerar en samling av en[`ChartSeries`](../chartseries/) .

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Returnerar antalet[`ChartSeries`](../chartseries/) i den här samlingen. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Returnerar en[`ChartSeries`](../chartseries/) vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[]*) | Lägger till nya[`ChartSeries`](../chartseries/) till den här samlingen. Använd den här metoden för att lägga till serier i histogramdiagram. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, ChartMultilevelValue[], double[]*) | Lägger till nya[`ChartSeries`](../chartseries/)till den här samlingen. Använd den här metoden för att lägga till serier som har datakategorier på flera nivåer. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_4)(*string, DateTime[], double[]*) | Lägger till nya[`ChartSeries`](../chartseries/) till den här samlingen. Använd den här metoden för att lägga till serier till alla typer av area-, radar- och aktiediagram. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, double[], double[]*) | Lägger till nya[`ChartSeries`](../chartseries/) till den här samlingen. Använd den här metoden för att lägga till serier i alla typer av punktdiagram. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_5)(*string, string[], double[]*) | Lägger till nya[`ChartSeries`](../chartseries/) till den här samlingen. Använd den här metoden för att lägga till serier i alla typer av stapel-, kolumn-, linje- och ytdiagram. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, double[], double[], double[]*) | Lägger till nya[`ChartSeries`](../chartseries/) till den här samlingen. Använd den här metoden för att lägga till serier i alla typer av bubbeldiagram. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_6)(*string, string[], double[], bool[]*) | Lägger till nya[`ChartSeries`](../chartseries/) till den här samlingen. Använd den här metoden för att lägga till serier i vattenfallsdiagram. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Tar bort alla[`ChartSeries`](../chartseries/) från den här samlingen. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Tar bort en[`ChartSeries`](../chartseries/) vid det angivna indexet. |

## Exempel

Visar hur man lägger till och tar bort seriedata i ett diagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett kolumndiagram som som standard innehåller tre serier med demodata.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Varje serie har fyra decimalvärden: ett för var och en av de fyra kategorierna.
// Fyra kluster med tre kolumner representerar dessa data.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Skriv namnet på varje serie i diagrammet.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Detta är namnen på kategorierna i diagrammet.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Vi kan lägga till en serie med nya värden för befintliga kategorier.
// Detta diagram kommer nu att innehålla fyra kluster med fyra kolumner.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// En diagramserie kan också tas bort med index, så här.
// Detta tar bort en av de tre demoserier som följde med diagrammet.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Vi kan också rensa all data i diagrammet på en gång med den här metoden.
// När du skapar ett nytt diagram är det här sättet att radera all demodata
// innan vi kan börja arbeta med ett tomt diagram.
chartData.Clear();
```

### Se även

* class [ChartSeries](../chartseries/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
