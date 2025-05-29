---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words för .NET
description: Upptäck metoden ChartXValue FromString för att enkelt skapa ChartXValue-instanser av strängtyp. Förbättra din datavisualisering idag!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Skapar en[`ChartXValue`](../) exempel påString typ.

```csharp
public static ChartXValue FromString(string value)
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

* class [ChartXValue](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
