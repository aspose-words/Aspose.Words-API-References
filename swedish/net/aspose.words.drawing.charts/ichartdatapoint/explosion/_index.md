---
title: IChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IChartDataPoint Explosion för cirkeldiagram. Kontrollera datapunktspositionering med precision – förbättra din visuella databerättelse idag!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Anger hur mycket datapunkten ska flyttas från cirkeldiagrammets mitt. Kan vara negativ, negativ betyder att egenskapen inte är angiven och ingen explosion ska tillämpas. Gäller endast cirkeldiagram.

```csharp
public int Explosion { get; set; }
```

## Exempel

Visar hur man flyttar utdelningssegmenten i ett cirkeldiagram bort från mitten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// "Skivor" av ett cirkeldiagram kan flyttas bort från mitten med hjälp av respektive datapunkts Explosion-attribut.
// Lägg till en datapunkt i den första delen av cirkeldiagrammet och flytta den 10 punkter bort från mitten.
// Aspose.Words skapar datapunkter automatiskt om de inte existerar.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Förskjut den andra delen med ett större avstånd.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Se även

* interface [IChartDataPoint](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
