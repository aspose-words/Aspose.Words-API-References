---
title: AxisDisplayUnit Class
linktitle: AxisDisplayUnit
articleTitle: AxisDisplayUnit
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.AxisDisplayUnit för att anpassa skalningsalternativ för värdeaxeln för förbättrad tydlighet och precision i diagram.
type: docs
weight: 790
url: /sv/net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

Ger åtkomst till skalningsalternativen för visningsenheterna för värdeaxeln.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class AxisDisplayUnit
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | Hämtar eller ställer in en användardefinierad divisor för att skala visningsenheter på värdeaxeln. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | Returnerar dokumentet som innehåller det överordnade diagrammet. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | Hämtar eller ställer in skalningsvärdet för visningsenheterna som ett av de fördefinierade värdena. |

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
