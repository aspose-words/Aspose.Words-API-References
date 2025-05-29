---
title: ChartAxis.DisplayUnit
linktitle: DisplayUnit
articleTitle: DisplayUnit
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ChartAxis DisplayUnit förbättrar din datavisualisering genom att optimera skalning av värdeaxeln för tydligare insikter.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartaxis/displayunit/
---
## ChartAxis.DisplayUnit property

Anger skalningsvärdet för visningsenheterna för värdeaxeln.

```csharp
public AxisDisplayUnit DisplayUnit { get; }
```

## Anmärkningar

Egenskapen har endast effekt för värdeaxlar.

## Exempel

Visar hur man manipulerar skalstreck och visade värden på en diagramaxel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Ställ in de mindre skalmarkeringarna på Y-axeln så att de pekar bort från plottområdet,
// och de stora skalmarkeringarna som korsar axeln.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Ställ in Y-axeln för att visa en större tick var 10:e enhet och en mindre tick var 1:e enhet.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Sätt Y-axelns gränser till -10 och 20.
// Denna Y-axel kommer nu att visa 4 större skalmärken och 27 mindre skalmärken.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// För X-axeln, sätt de stora skalmarkeringarna var 10:e enhet,
// varje mindre bockmarkering vid 2,5 enheter.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Konfigurera båda typerna av skalstreck så att de visas inuti grafens plottområde.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Ställ in X-axelns gränser så att X-axeln sträcker sig över 5 större skalmärken och 12 mindre skalmärken.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Ställ in kryssrutorna så att de visar deras värde i miljoner.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Vi kan ställa in ett mer specifikt värde med vilket tick-etiketter visar sina värden.
// Detta påstående motsvarar det ovanstående.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Se även

* class [AxisDisplayUnit](../../axisdisplayunit/)
* class [ChartAxis](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
