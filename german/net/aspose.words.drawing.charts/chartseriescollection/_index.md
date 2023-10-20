---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection klas. Stellt eine Sammlung von a darChartSeries  in C#.
type: docs
weight: 790
url: /de/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Stellt eine Sammlung von a dar[`ChartSeries`](../chartseries/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Gibt die Anzahl zurück[`ChartSeries`](../chartseries/) in dieser Sammlung. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Gibt a zurück[`ChartSeries`](../chartseries/) am angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, DateTime[], double[]*) | Fügt Neues hinzu[`ChartSeries`](../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Serien zu jeder Art von Flächen-, Radar- und Aktiendiagrammen hinzuzufügen. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, double[], double[]*) | Fügt Neues hinzu[`ChartSeries`](../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu jeder Art von Streudiagrammen hinzuzufügen. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, string[], double[]*) | Fügt Neues hinzu[`ChartSeries`](../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu jeder Art von Balken-, Säulen-, Linien- und Oberflächendiagrammen hinzuzufügen. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[], double[], double[]*) | Fügt Neues hinzu[`ChartSeries`](../chartseries/)zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu jeder Art von Blasendiagrammen hinzuzufügen. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Entfernt alle[`ChartSeries`](../chartseries/) aus dieser Sammlung. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Entfernt a[`ChartSeries`](../chartseries/) am angegebenen Index. |

## Beispiele

Zeigt, wie man Reihendaten in einem Diagramm hinzufügt und entfernt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Säulendiagramm einfügen, das standardmäßig drei Serien von Demodaten enthält.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Jede Reihe hat vier Dezimalwerte: einen für jede der vier Kategorien.
// Vier Cluster mit drei Spalten stellen diese Daten dar.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Den Namen jeder Serie im Diagramm ausgeben.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Dies sind die Namen der Kategorien im Diagramm.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Wir können eine Reihe mit neuen Werten für bestehende Kategorien hinzufügen.
// Dieses Diagramm enthält jetzt vier Cluster mit vier Spalten.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Eine Diagrammreihe kann auch wie folgt nach Index entfernt werden.
// Dadurch wird eine der drei Demoserien entfernt, die mit dem Diagramm geliefert wurden.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Mit dieser Methode können wir auch alle Daten des Diagramms auf einmal löschen.
// Beim Erstellen eines neuen Diagramms werden auf diese Weise alle Demodaten gelöscht
// bevor wir mit der Arbeit an einem leeren Diagramm beginnen können.
chartData.Clear();
```

### Siehe auch

* class [ChartSeries](../chartseries/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
