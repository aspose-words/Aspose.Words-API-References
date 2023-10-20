---
title: AxisBuiltInUnit Enum
linktitle: AxisBuiltInUnit
articleTitle: AxisBuiltInUnit
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Charts.AxisBuiltInUnit uppräkning. Anger visningsenheterna för en axel i C#.
type: docs
weight: 520
url: /sv/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

Anger visningsenheterna för en axel.

```csharp
public enum AxisBuiltInUnit
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Anger värdena på diagrammet som ska visas som de är. |
| Custom | `1` | Anger att värdena på diagrammet ska delas med en användardefinierad divisor. Detta värde stöds inte av de nya diagramtyperna i MS Office 2016. |
| Billions | `2` | Anger att värdena på diagrammet ska delas med 1 000 000 000. |
| HundredMillions | `3` | Anger att värdena i diagrammet ska delas med 100 000 000. |
| Hundreds | `4` | Anger att värdena på diagrammet ska delas med 100. |
| HundredThousands | `5` | Anger att värdena på diagrammet ska delas med 100 000. |
| Millions | `6` | Anger att värdena på diagrammet ska delas med 1 000 000. |
| TenMillions | `7` | Anger att värdena i diagrammet ska delas med 10 000 000. |
| TenThousands | `8` | Anger att värdena på diagrammet ska delas med 10 000. |
| Thousands | `9` | Anger att värdena på diagrammet ska delas med 1 000. |
| Trillions | `10` | Anger att värdena på diagrammet ska delas med 1 000 000 000 0000. |
| Percentage | `11` | Anger att värdena på diagrammet ska delas med 0,01. Detta värde stöds endast av de nya diagram -typerna av MS Office 2016. |

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
