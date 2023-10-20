---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Charts.ChartYValueCollection klas. Stellt eine Sammlung von YWerten für eine Diagrammreihe dar in C#.
type: docs
weight: 880
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
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Ruft den Y-Wert am angegebenen Index ab oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

## Bemerkungen

Alle Objekte der Sammlung außer**Null** muss das Gleiche haben[`ValueType`](../chartyvalue/valuetype/).

Die Sammlung erlaubt nur das Ändern von Y-Werten. Um einer Diagrammreihe neue Werte hinzuzufügen oder einzufügen oder Werte zu entfernen, verwenden Sie die entsprechenden Methoden der[`ChartSeries`](../chartseries/) Klasse verwendet werden kann.

## Beispiele

Zeigt, wie man Diagrammseriendaten erhält.

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
    // Individuelles Format aller Datenpunkte löschen.
    // Datenpunkte und Datenwerte stehen in Säulendiagrammen eins zu eins.
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

// Farben der Max- und Min-Werte ändern.
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
