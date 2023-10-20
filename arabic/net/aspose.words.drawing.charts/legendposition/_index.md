---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.LegendPosition تعداد. يحدد المواضع المحتملة لوسيلة إيضاح المخطط في C#.
type: docs
weight: 910
url: /ar/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

يحدد المواضع المحتملة لوسيلة إيضاح المخطط.

```csharp
public enum LegendPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لن يتم عرض وسيلة إيضاح للمخطط. |
| Bottom | `1` | يحدد أنه سيتم رسم وسيلة الإيضاح في أسفل المخطط. |
| Left | `2` | يحدد أنه سيتم رسم وسيلة الإيضاح على يسار المخطط. |
| Right | `3` | يحدد أنه سيتم رسم وسيلة الإيضاح على يمين المخطط. |
| Top | `4` | يحدد أنه يجب رسم وسيلة الإيضاح في أعلى المخطط. |
| TopRight | `5` | يحدد أنه سيتم رسم وسيلة الإيضاح في أعلى يمين المخطط. |

## أمثلة

يوضح كيفية تحرير مظهر وسيلة إيضاح المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// انقل وسيلة إيضاح المخطط إلى الزاوية اليمنى العليا.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// امنح عناصر المخطط الأخرى، مثل الرسم البياني، مساحة أكبر من خلال السماح لها بتداخل وسيلة الإيضاح.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
