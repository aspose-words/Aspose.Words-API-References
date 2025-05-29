---
title: ChartXValueCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words für .NET
description: Entdecken Sie die FormatCode-Eigenschaft von ChartXValueCollection und passen Sie X-Wertformate einfach an, um die Datenvisualisierung und Übersichtlichkeit Ihrer Diagramme zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartxvaluecollection/formatcode/
---
## ChartXValueCollection.FormatCode property

Ruft den auf die X-Werte angewendeten Formatcode ab oder legt ihn fest.

```csharp
public string FormatCode { get; set; }
```

## Bemerkungen

Die Zahlenformatierung wird verwendet, um die Darstellung von Werten im Diagramm zu ändern. Beispiele für Zahlenformate:

Zahl - "#,##0.00"

Währung - "\"$\"#,##0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "t/mm/jjjj"

Prozentsatz - "0,00 %"

Bruch - "# ?/?"

Wissenschaftlich - "0.00E+00"

Buchhaltung - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Benutzerdefiniert mit Farbe – „[Rot]-#,##0.0“

## Beispiele

Zeigt, wie mit dem Formatcode der Diagrammdaten gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Blasendiagramm ein.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Datenformatcodes festlegen.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Siehe auch

* class [ChartXValueCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
