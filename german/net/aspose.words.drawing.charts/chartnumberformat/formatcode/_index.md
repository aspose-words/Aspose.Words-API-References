---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der FormatCode-Eigenschaft von ChartNumberFormat Datenbeschriftungsformate anpassen können, um klarere Einblicke und eine verbesserte Datenpräsentation zu erzielen.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Ruft den auf eine Datenbeschriftung angewendeten Formatcode ab oder legt ihn fest.

```csharp
public string FormatCode { get; set; }
```

## Bemerkungen

Die Zahlenformatierung wird verwendet, um die Darstellung eines Werts in einer Datenbeschriftung zu ändern und kann auf sehr kreative Weise eingesetzt werden. Beispiele für Zahlenformate:

Zahl - "#,##0.00"

Währung - "\"$\"#,##0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "t/mm/jjjj"

Prozentsatz - "0,00 %"

Bruch - "# ?/?"

Wissenschaftlich - "0.00E+00"

Text - "@"

Buchhaltung - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Benutzerdefiniert mit Farbe – „[Rot]-#,##0.0“

## Beispiele

Zeigt, wie die Formatierung für Diagrammwerte festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie dem Diagramm eine benutzerdefinierte Reihe mit Kategorien für die X-Achse hinzu,
    // und große entsprechende numerische Werte für die Y-Achse.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

    // Legen Sie das Zahlenformat der Teilstrichbeschriftungen der Y-Achse so fest, dass Ziffern nicht durch Kommas gruppiert werden.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Dieses Flag kann den obigen Wert überschreiben und das Zahlenformat aus der Quellzelle übernehmen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

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

* class [ChartNumberFormat](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
