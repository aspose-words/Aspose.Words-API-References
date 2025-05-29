---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Greifen Sie mit der Schriftarteigenschaft ChartDataLabelCollection auf die Schriftformatierung der Datenbeschriftungen Ihrer gesamten Serie zu und passen Sie diese an, um die Datenvisualisierung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Bietet Zugriff auf die Schriftformatierung der Datenbeschriftungen der gesamten Serie.

```csharp
public Font Font { get; }
```

## Bemerkungen

Der für diese Eigenschaft definierte Wert kann für ein einzelnes Datenlabel mit dem überschrieben werden.[`Font`](../../chartdatalabel/font/) Eigenschaft.

## Beispiele

Zeigt, wie Datenbeschriftungen für eine Diagrammreihe aktiviert und konfiguriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Liniendiagramm hinzu und löschen Sie dann die Demo-Datenreihe, um mit einem sauberen Diagramm zu beginnen.
// und dann einen Titel festlegen.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Fügen Sie eine benutzerdefinierte Diagrammreihe mit Monaten als Kategorien für die X-Achse ein,
// und entsprechende Dezimalbeträge für die Y-Achse.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// Aktivieren Sie Datenbeschriftungen und wenden Sie dann ein benutzerdefiniertes Zahlenformat für die in den Datenbeschriftungen angezeigten Werte an.
// Dieses Format behandelt angezeigte Dezimalwerte als Millionen US-Dollar.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Siehe auch

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
