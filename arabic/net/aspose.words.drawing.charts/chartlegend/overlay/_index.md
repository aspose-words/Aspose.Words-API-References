---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words لـ .NET
description: تداخل عناصر مخطط التحكم مع خاصية تراكب أسطورة الرسم البياني. حسّن تصوّر بياناتك بإعدادات أسطورة قابلة للتخصيص للحصول على رؤى أوضح.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

يحدد ما إذا كان سيتم السماح لعناصر الرسم البياني الأخرى بالتداخل مع الأسطورة. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool Overlay { get; set; }
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

* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
