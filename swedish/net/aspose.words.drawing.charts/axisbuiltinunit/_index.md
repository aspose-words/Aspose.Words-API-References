---
title: AxisBuiltInUnit Enum
linktitle: AxisBuiltInUnit
articleTitle: AxisBuiltInUnit
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.Charts.AxisBuiltInUnit-uppräkningen för anpassningsbara axelvisningsenheter, vilket förbättrar ditt diagrams tydlighet och effektivitet.
type: docs
weight: 760
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
| None | `0` | Anger att värdena i diagrammet ska visas som de är. |
| Custom | `1` | Anger att värdena i diagrammet ska divideras med en användardefinierad divisor. Detta värde stöds inte av de nya diagramtyperna i MS Office 2016. |
| Billions | `2` | Anger att värdena i diagrammet ska divideras med 1 000 000 000. |
| HundredMillions | `3` | Anger att värdena i diagrammet ska divideras med 100 000 000. |
| Hundreds | `4` | Anger att värdena i diagrammet ska divideras med 100. |
| HundredThousands | `5` | Anger att värdena i diagrammet ska divideras med 100 000. |
| Millions | `6` | Anger att värdena i diagrammet ska divideras med 1 000 000. |
| TenMillions | `7` | Anger att värdena i diagrammet ska divideras med 10 000 000. |
| TenThousands | `8` | Anger att värdena i diagrammet ska divideras med 10 000. |
| Thousands | `9` | Anger att värdena i diagrammet ska divideras med 1 000. |
| Trillions | `10` | Anger att värdena i diagrammet ska divideras med 1 000 000 000 000. |
| Percentage | `11` | Anger att värdena i diagrammet ska divideras med 0,01. Detta värde stöds endast av de nya chart -typerna i MS Office 2016. |

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
