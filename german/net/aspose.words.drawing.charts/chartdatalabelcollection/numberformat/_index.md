---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die NumberFormat-Eigenschaft der ChartDataLabelCollection, um Datenbeschriftungsformate für Ihre gesamte Serie einfach anzupassen und so die Übersichtlichkeit und Präsentation zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Erhält eine[`ChartNumberFormat`](../../chartnumberformat/) Instanz, die das Festlegen des Zahlenformats für die Datenbeschriftungen der gesamten Serie ermöglicht.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
