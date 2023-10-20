---
title: ChartAxis.TickLabelAlignment
linktitle: TickLabelAlignment
articleTitle: TickLabelAlignment
second_title: Aspose.Words för .NET
description: ChartAxis TickLabelAlignment fast egendom. Hämtar eller ställer in textjustering av axelmarkeringsetiketter i C#.
type: docs
weight: 220
url: /sv/net/aspose.words.drawing.charts/chartaxis/ticklabelalignment/
---
## ChartAxis.TickLabelAlignment property

Hämtar eller ställer in textjustering av axelmarkeringsetiketter.

```csharp
public ParagraphAlignment TickLabelAlignment { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt för etiketter med flera rader.

Standardvärdet ärCenter.

.

## Exempel

Visar hur man manipulerar bockmarkeringarna och visade värden för en diagramaxel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Ställ in de mindre bockarna på Y-axeln så att de pekar bort från plotområdet,
// och de stora bockarna för att korsa axeln.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Ställ in Y-axeln så att den visar en större bock var 10:e enhet, och en mindre bock var 1:e enhet.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Ställ in Y-axelns gränser till -10 och 20.
// Den här Y-axeln kommer nu att visa 4 större tick-markeringar och 27 mindre tick-markeringar.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// För X-axeln, ställ in de viktigaste bockmarkeringarna på var 10:e enhet,
// varje mindre bock vid 2,5 enheter.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Konfigurera båda typerna av bockmarkeringar så att de visas inuti diagramområdet.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Ställ in X-axelns gränser så att X-axeln sträcker sig över 5 större markeringar och 12 mindre markeringar.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Ställ in markeringarna så att de visar deras värde i miljoner.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Vi kan ställa in ett mer specifikt värde med vilket bocketiketter ska visa sina värden.
// Detta påstående är likvärdigt med det ovan.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Se även

* enum [ParagraphAlignment](../../../aspose.words/paragraphalignment/)
* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
