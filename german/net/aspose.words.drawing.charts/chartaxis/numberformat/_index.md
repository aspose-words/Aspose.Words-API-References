---
title: ChartAxis.NumberFormat
second_title: Aspose.Words für .NET-API-Referenz
description: ChartAxis eigendom. Gibt a zurückChartNumberFormat Objekt das die Definition von Zahlenformaten für die Achse ermöglicht.
type: docs
weight: 190
url: /de/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Gibt a zurück[`ChartNumberFormat`](../../chartnumberformat/) Objekt, das die Definition von Zahlenformaten für die Achse ermöglicht.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Beispiele

Zeigt, wie die Formatierung für Diagrammwerte festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Dem Diagramm eine benutzerdefinierte Reihe mit Kategorien für die X-Achse hinzufügen,
 // und große jeweilige numerische Werte für die Y-Achse.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Stellen Sie das Zahlenformat der Y-Achsen-Teilstrichbeschriftungen so ein, dass Ziffern nicht mit Kommas gruppiert werden.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Dieses Flag kann den obigen Wert überschreiben und das Zahlenformat aus der Quellzelle ziehen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Siehe auch

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartaxis/)
* Montage [Aspose.Words](../../../)


