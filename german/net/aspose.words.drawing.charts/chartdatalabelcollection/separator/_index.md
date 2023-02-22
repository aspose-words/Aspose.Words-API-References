---
title: ChartDataLabelCollection.Separator
second_title: Aspose.Words für .NET-API-Referenz
description: ChartDataLabelCollection eigendom. Ermittelt oder setzt Zeichenfolgentrennzeichen die für die Datenbeschriftungen der gesamten Serie verwendet werden. Der Standardwert ist ein Komma außer bei Tortendiagrammen die nur den Kategorienamen und den Prozentsatz anzeigen wenn stattdessen ein Zeilenumbruch verwendet werden soll.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Ermittelt oder setzt Zeichenfolgentrennzeichen, die für die Datenbeschriftungen der gesamten Serie verwendet werden. Der Standardwert ist ein Komma, außer bei Tortendiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, wenn stattdessen ein Zeilenumbruch verwendet werden soll.

```csharp
public string Separator { get; set; }
```

### Bemerkungen

Der für diese Eigenschaft definierte Wert kann für eine einzelne Datenbeschriftung mit der Verwendung von überschrieben werden.[`Separator`](../../chartdatalabel/separator/) Eigentum.

### Beispiele

Zeigt, wie mit Datenbeschriftungen eines Blasendiagramms gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

 // Fügen Sie eine benutzerdefinierte Serie mit X/Y-Koordinaten und Durchmesser jeder Blase hinzu.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Datenbeschriftungen aktivieren und dann deren Aussehen ändern.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

Zeigt, wie Sie mit Datenbeschriftungen eines Kreisdiagramms arbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine benutzerdefinierte Diagrammreihe mit einem Kategorienamen für jeden der Sektoren und deren Häufigkeitstabelle ein.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Aktivieren Sie Datenbeschriftungen, die sowohl den Prozentsatz als auch die Häufigkeit jedes Sektors anzeigen, und ändern Sie deren Aussehen.
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
* namensraum [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* Montage [Aspose.Words](../../../)


