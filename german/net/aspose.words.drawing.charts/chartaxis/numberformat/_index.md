---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChartAxis NumberFormat“, um die Zahlenformate Ihres Diagramms mühelos mit dem Objekt „ChartNumberFormat“ für eine verbesserte Datenvisualisierung anzupassen.
type: docs
weight: 200
url: /de/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Gibt einen[`ChartNumberFormat`](../../chartnumberformat/) Objekt, mit dem Zahlenformate für die Achse definiert werden können.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
