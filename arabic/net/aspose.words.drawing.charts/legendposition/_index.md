---
title: Enum LegendPosition
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.LegendPosition تعداد. يحدد المواضع المحتملة لوسيلة إيضاح الرسم البياني.
type: docs
weight: 780
url: /ar/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

يحدد المواضع المحتملة لوسيلة إيضاح الرسم البياني.

```csharp
public enum LegendPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لن يتم عرض وسيلة إيضاح للرسم البياني . |
| Bottom | `1` | يحدد أن وسيلة الإيضاح سيتم رسمها في أسفل الرسم البياني. |
| Left | `2` | يحدد أن وسيلة الإيضاح سيتم رسمها على يسار الرسم البياني. |
| Right | `3` | يحدد أن وسيلة الإيضاح سيتم رسمها على يمين الرسم البياني. |
| Top | `4` | يحدد أن وسيلة الإيضاح سيتم رسمها أعلى المخطط. |
| TopRight | `5` | يحدد أن وسيلة الإيضاح سيتم رسمها في أعلى يمين الرسم البياني. |

### أمثلة

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

// انقل وسيلة إيضاح الرسم البياني إلى الزاوية اليمنى العليا.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// امنح عناصر المخطط الأخرى ، مثل الرسم البياني ، مساحة أكبر من خلال السماح لهم بالتداخل مع وسيلة الإيضاح.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


