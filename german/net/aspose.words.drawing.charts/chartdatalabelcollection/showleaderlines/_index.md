---
title: ChartDataLabelCollection.ShowLeaderLines
second_title: Aspose.Words für .NET-API-Referenz
description: ChartDataLabelCollection eigendom. Ermöglicht die Angabe ob Führungslinien für Datenbeschriftungen für die Datenbeschriftungen der gesamten Serie angezeigt werden müssen. Der Standardwert istFALSCH .
type: docs
weight: 100
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

Ermöglicht die Angabe, ob Führungslinien für Datenbeschriftungen für die Datenbeschriftungen der gesamten Serie angezeigt werden müssen. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowLeaderLines { get; set; }
```

### Bemerkungen

Gilt nur für Kreisdiagramme. Führungslinien stellen eine visuelle Verbindung zwischen einer Datenbeschriftung und dem entsprechenden Datenpunkt her.

Der für diese Eigenschaft definierte Wert kann für eine einzelne Datenbeschriftung mithilfe von the überschrieben werden.[`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) Eigentum.

### Beispiele

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
* namensraum [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* Montage [Aspose.Words](../../../)


