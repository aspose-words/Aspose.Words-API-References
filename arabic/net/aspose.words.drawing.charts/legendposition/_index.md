---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.Charts.LegendPosition لتخصيص موضع أسطورة الرسم البياني بسهولة لتحسين تصور البيانات.
type: docs
weight: 1230
url: /ar/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

يحدد المواضع المحتملة لأسطورة الرسم البياني.

```csharp
public enum LegendPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لن يتم عرض أي أسطورة للرسم البياني. |
| Bottom | `1` | يحدد أنه يجب رسم الأسطورة في أسفل الرسم البياني. |
| Left | `2` | يحدد أنه يجب رسم الأسطورة على يسار الرسم البياني. |
| Right | `3` | يحدد أنه يجب رسم الأسطورة على يمين الرسم البياني. |
| Top | `4` | يحدد أنه يجب رسم الأسطورة في الجزء العلوي من الرسم البياني. |
| TopRight | `5` | يحدد أنه يجب رسم الأسطورة في الجزء العلوي الأيمن من الرسم البياني. |

## أمثلة

يوضح كيفية تحرير مظهر أسطورة الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// نقل أسطورة الرسم البياني إلى الزاوية اليمنى العليا.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// امنح عناصر الرسم البياني الأخرى، مثل الرسم البياني، مساحة أكبر من خلال السماح لها بالتداخل مع الأسطورة.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
