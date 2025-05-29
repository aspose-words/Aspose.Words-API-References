---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChartAxis Hidden“, um die Achsensichtbarkeit in Ihren Diagrammen einfach zu verwalten. Verbessern Sie Ihre Datenpräsentation mit dieser einfachen Umschaltfunktion!
type: docs
weight: 110
url: /de/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Ruft ein Flag ab oder legt es fest, das angibt, ob diese Achse ausgeblendet ist oder nicht.

```csharp
public bool Hidden { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt, wie Diagrammachsen ausgeblendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine benutzerdefinierte Reihe mit Kategorien für die X-Achse und entsprechenden Dezimalwerten für die Y-Achse hinzu.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

    // Blenden Sie die Diagrammachsen aus, um die Darstellung des Diagramms zu vereinfachen.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Siehe auch

* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
