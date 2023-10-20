---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words لـ .NET
description: ChartLegend Overlay ملكية. يحدد ما إذا كان سيتم السماح لعناصر المخطط الأخرى بتداخل وسيلة الإيضاح أم لا. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

يحدد ما إذا كان سيتم السماح لعناصر المخطط الأخرى بتداخل وسيلة الإيضاح أم لا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
