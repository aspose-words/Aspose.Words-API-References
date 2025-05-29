---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartNumberFormat für erweiterte Zahlenformatierung in Diagrammen. Verbessern Sie die visuelle Attraktivität Ihres Dokuments!
type: docs
weight: 1060
url: /de/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Stellt die Zahlenformatierung des übergeordneten Elements dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartNumberFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Ruft den auf eine Datenbeschriftung angewendeten Formatcode ab oder legt ihn fest. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. Der Standardwert ist „true“. |

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

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
