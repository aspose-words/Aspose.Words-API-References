---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartAxis AxisBetweenCategories – kontrollera värdeaxelns positionering för förbättrad kategorivisualisering i dina diagram. Optimera din datapresentation!
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Hämtar eller ställer in en flagga som anger om värdeaxeln korsar kategoriaxeln mellan kategorier.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Anmärkningar

Egenskapen har endast effekt för värdeaxlar. Den stöds inte av nya diagram i MS Office 2016.

## Exempel

Visar hur man får en grafaxel att korsa vid en anpassad plats.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// För stapeldiagram korsar Y-axeln vid noll som standard,
// vilket innebär att kolumner för alla värden under noll pekar nedåt för att representera negativa värden.
// Vi kan ställa in ett annat värde för Y-axelns korsning. I det här fallet ställer vi in det till 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Se även

* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
