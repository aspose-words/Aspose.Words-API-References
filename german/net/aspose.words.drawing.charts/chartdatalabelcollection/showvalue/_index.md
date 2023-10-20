---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words für .NET
description: ChartDataLabelCollection ShowValue eigendom. Ermöglicht die Angabe ob Werte in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Der Standardwert istFALSCH  in C#.
type: docs
weight: 140
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowValue { get; set; }
```

## Bemerkungen

Der für diese Eigenschaft definierte Wert kann für eine einzelne Datenbeschriftung mithilfe von überschrieben werden.[`ShowValue`](../../chartdatalabel/showvalue/) Eigenschaft.

## Beispiele

Zeigt, wie mit Datenbeschriftungen eines Kreisdiagramms gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine benutzerdefinierte Diagrammreihe mit einem Kategorienamen für jeden Sektor und deren Häufigkeitstabelle ein.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Aktivieren Sie Datenbeschriftungen, die sowohl den Prozentsatz als auch die Häufigkeit jedes Sektors anzeigen, und ändern Sie deren Erscheinungsbild.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Siehe auch

* class [ChartDataLabelCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
