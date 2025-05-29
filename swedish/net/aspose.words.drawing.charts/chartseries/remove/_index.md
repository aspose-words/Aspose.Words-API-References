---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Ta enkelt bort X-värden, Y-värden och bubbelstorlekar från dina diagramserier med metoden ChartSeries Remove. Effektivisera din datavisualisering idag!
type: docs
weight: 210
url: /sv/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Tar bort X-värdet, Y-värdet och bubbelstorleken, om det stöds, från diagramserien vid det angivna indexet. Motsvarande datapunkt och dataetikett tas också bort.

```csharp
public void Remove(int index)
```

## Exempel

Visar hur man lägger till/tar bort datavärden i diagrammet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Ta bort det första värdet i båda serierna.
department1Series.Remove(0);
department2Series.Remove(0);

// Lägg till nya värden i båda serierna.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Se även

* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
