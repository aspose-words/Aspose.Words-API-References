---
title: ChartSeriesCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Upptäck ChartSeriesCollection GetEnumerator-metoden – hämta effektivt uppräknarobjekt för sömlös datamanipulation och analys.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartseriescollection/getenumerator/
---
## ChartSeriesCollection.GetEnumerator method

Returnerar ett uppräknarobjekt.

```csharp
public IEnumerator<ChartSeries> GetEnumerator()
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
