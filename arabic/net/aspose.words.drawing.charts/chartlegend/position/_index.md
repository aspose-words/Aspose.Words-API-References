---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية موضع ChartLegend لتخصيص موضع أسطورة الرسم البياني الخاص بك بسهولة لتحسين الوضوح والجاذبية البصرية.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

يحدد موضع الأسطورة على الرسم البياني.

```csharp
public LegendPosition Position { get; set; }
```

## ملاحظات

القيمة الافتراضية هيRight لمخططات ما قبل Word 2016 و Top لمخططات Word 2016.

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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
