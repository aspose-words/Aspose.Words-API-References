---
title: ChartSeriesCollection.Count
second_title: Aspose.Words för .NET API Referens
description: ChartSeriesCollection fast egendom. Returnerar antaletChartSeries i den här samlingen.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartseriescollection/count/
---
## ChartSeriesCollection.Count property

Returnerar antalet[`ChartSeries`](../../chartseries/) i den här samlingen.

```csharp
public int Count { get; }
```

### Exempel

Visar hur man lägger till och tar bort seriedata i ett diagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett kolumndiagram som kommer att innehålla tre serier av demodata som standard.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Varje serie har fyra decimalvärden: ett för var och en av de fyra kategorierna.
// Fyra kluster med tre kolumner kommer att representera denna data.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Skriv ut namnet på varje serie i diagrammet.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Det här är namnen på kategorierna i diagrammet.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Vi kan lägga till en serie med nya värden för befintliga kategorier.
// Detta diagram kommer nu att innehålla fyra kluster med fyra kolumner.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// En diagramserie kan också tas bort med index, så här.
// Detta tar bort en av de tre demoserierna som följde med diagrammet.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Vi kan också rensa alla diagrammets data på en gång med den här metoden.
// När du skapar ett nytt diagram är det här sättet att torka all demodata
// innan vi kan börja arbeta på ett tomt diagram.
chartData.Clear();
```

### Se även

* class [ChartSeriesCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* hopsättning [Aspose.Words](../../../)


