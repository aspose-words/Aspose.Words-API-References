---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "أسطورة الرسم البياني" لتخصيص مخططاتك بسهولة. حسّن تصوّر البيانات بخيارات أسطورة مُصمّمة خصيصًا لرؤى أفضل!
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

يوفر الوصول إلى خصائص أسطورة الرسم البياني.

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
