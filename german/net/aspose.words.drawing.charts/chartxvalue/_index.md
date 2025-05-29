---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartXValue, Ihre Lösung zum Definieren von X-Werten in Diagrammreihen und zur mühelosen Verbesserung der Datenvisualisierung.
type: docs
weight: 1160
url: /de/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Stellt einen X-Wert für eine Diagrammreihe dar.

```csharp
public class ChartXValue
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Ruft den gespeicherten Datums-/Uhrzeitwert ab. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Ruft den gespeicherten numerischen Wert ab. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Ruft den gespeicherten mehrstufigen Wert ab. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Ruft den gespeicherten Zeichenfolgenwert ab. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Ruft den gespeicherten Zeitwert ab. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Ruft den Typ des im Objekt gespeicherten X-Werts ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Erstellt eine`ChartXValue` Instanz derDateTime Typ. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Erstellt eine`ChartXValue` Instanz derDouble Typ. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Erstellt eine`ChartXValue` Instanz derMultilevel Typ. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Erstellt eine`ChartXValue` Instanz derString Typ. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Erstellt eine`ChartXValue` Instanz derTime Typ. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Ruft ein Flag ab, das angibt, ob das angegebene Objekt dem aktuellen X-Wert-Objekt entspricht. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Ruft einen Hashcode für das aktuelle X-Wertobjekt ab. |

## Bemerkungen

Diese Klasse enthält eine Reihe statischer Methoden zum Erstellen eines X-Wertes eines bestimmten Typs. The [`ValueType`](./valuetype/) Mit der Eigenschaft können Sie den Typ eines vorhandenen X-Werts bestimmen.

Alle X-Werte einer Diagrammreihe, die nicht Null sind, müssen gleich sein[`ChartXValueType`](../chartxvaluetype/) Typ.

## Beispiele

Zeigt, wie Diagrammreihen mit Daten gefüllt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// X- und Y-Werte der ersten Reihe löschen.
series1.ClearValues();

// Fülle die Reihe mit Daten.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// X- und Y-Werte der zweiten Reihe löschen.
series2.Clear();

// Fülle die Reihe mit Daten.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
