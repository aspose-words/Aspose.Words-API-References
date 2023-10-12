---
title: Class ChartXValueCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartXValueCollection klas. Stellt eine Sammlung von XWerten für eine Diagrammreihe dar.
type: docs
weight: 850
url: /de/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Stellt eine Sammlung von X-Werten für eine Diagrammreihe dar.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Ruft die Anzahl der Elemente in dieser Sammlung ab. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Ruft den X-Wert am angegebenen Index ab oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

### Bemerkungen

Alle Objekte der Sammlung außer **Null** muss das Gleiche haben[`ValueType`](../chartxvalue/valuetype/).

Die Sammlung erlaubt nur das Ändern von X-Werten. Um einer Diagrammreihe neue Werte hinzuzufügen oder einzufügen oder Werte zu entfernen, verwenden Sie die entsprechenden Methoden der[`ChartSeries`](../chartseries/) Klasse verwendet werden kann.

### Beispiele

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
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


