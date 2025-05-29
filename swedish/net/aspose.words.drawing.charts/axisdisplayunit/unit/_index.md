---
title: AxisDisplayUnit.Unit
linktitle: Unit
articleTitle: Unit
second_title: Aspose.Words för .NET
description: Upptäck egenskapen AxisDisplayUnit för att enkelt anpassa skalning av visningsenheter med fördefinierade värden för förbättrad datavisualisering.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/axisdisplayunit/unit/
---
## AxisDisplayUnit.Unit property

Hämtar eller ställer in skalningsvärdet för visningsenheterna som ett av de fördefinierade värdena.

```csharp
public AxisBuiltInUnit Unit { get; set; }
```

## Anmärkningar

Standardvärdet ärNone DenCustom och Percentage värden är inte tillgängliga i vissa diagramtyper; see [`AxisBuiltInUnit`](../../axisbuiltinunit/) för mer information.

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

* enum [AxisBuiltInUnit](../../axisbuiltinunit/)
* class [AxisDisplayUnit](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
