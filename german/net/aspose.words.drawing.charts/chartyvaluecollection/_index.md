---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartYValueCollection, Ihre Lösung für die effiziente und effektive Verwaltung von Y-Werten in Diagrammreihen.
type: docs
weight: 1200
url: /de/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

Stellt eine Sammlung von Y-Werten für eine Diagrammreihe dar.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Ruft die Anzahl der Elemente in dieser Sammlung ab. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | Ruft den auf die Y-Werte angewendeten Formatcode ab oder legt ihn fest. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Ruft den Y-Wert am angegebenen Index ab oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

## Bemerkungen

Alle Gegenstände der Sammlung außer**null** muss das gleiche haben[`ValueType`](../chartyvalue/valuetype/).

Die Sammlung erlaubt nur das Ändern von Y-Werten. Um einer Diagrammreihe neue Werte hinzuzufügen, einzufügen oder Werte zu entfernen, verwenden Sie die entsprechenden Methoden der[`ChartSeries`](../chartseries/) Klasse kann verwendet werden.

## Beispiele

Zeigt, wie man Diagrammreihendaten erhält.

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
    // Klares individuelles Format aller Datenpunkte.
    // Datenpunkte und Datenwerte sind in Säulendiagrammen eins zu eins.
    series.DataPoints[i].ClearFormat();

    // Y-Wert abrufen.
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

// Farben der Maximal- und Minimalwerte ändern.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Siehe auch

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
