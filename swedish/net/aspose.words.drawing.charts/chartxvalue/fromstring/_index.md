---
title: ChartXValue.FromString
second_title: Aspose.Words för .NET API Referens
description: ChartXValue metod. Skapar enChartXValue instans avString typ.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Skapar en[`ChartXValue`](../) instans avString typ.

```csharp
public static ChartXValue FromString(string value)
```

### Exempel

Visar hur man lägger till/tar bort diagramdatavärden.

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

// Lägg till nya värden till båda serierna.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Se även

* class [ChartXValue](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* hopsättning [Aspose.Words](../../../)


