---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „ChartNumberFormat IsLinkedToSource“ Ihre Datenvisualisierung durch die Verknüpfung von Formatcodes mit Quellzellen verbessert. Jetzt mehr erfahren!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. Der Standardwert ist „true“.

```csharp
public bool IsLinkedToSource { get; set; }
```

## Bemerkungen

Das NumberFormat wird auf „Allgemein“ zurückgesetzt, wenn der Formatcode mit der Quelle verknüpft ist.

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

* class [ChartNumberFormat](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
