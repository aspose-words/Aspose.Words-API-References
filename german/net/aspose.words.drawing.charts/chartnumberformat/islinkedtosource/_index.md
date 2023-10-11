---
title: ChartNumberFormat.IsLinkedToSource
second_title: Aspose.Words für .NET-API-Referenz
description: ChartNumberFormat eigendom. Gibt an ob der Formatcode mit einer Quellzelle verknüpft ist. Der Standardwert ist true.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. Der Standardwert ist true.

```csharp
public bool IsLinkedToSource { get; set; }
```

### Bemerkungen

Das NumberFormat wird auf „Allgemein“ zurückgesetzt, wenn der Formatcode mit der Quelle verknüpft ist.

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

* class [ChartNumberFormat](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartnumberformat/)
* Montage [Aspose.Words](../../../)


