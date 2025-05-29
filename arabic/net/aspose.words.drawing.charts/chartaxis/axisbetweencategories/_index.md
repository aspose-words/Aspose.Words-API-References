---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartAxis AxisBetweenCategories — للتحكم في موضع محور القيمة لتحسين عرض الفئات في مخططاتك. حسّن عرض بياناتك!
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

يحصل على علم أو يعينه للإشارة إلى ما إذا كان محور القيمة يعبر محور الفئة بين الفئات.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## ملاحظات

هذه الخاصية تنطبق فقط على محاور القيم. لا تدعمها مخططات MS Office 2016 الجديدة.

## أمثلة

يوضح كيفية جعل محور الرسم البياني يتقاطع في موقع مخصص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// بالنسبة للمخططات العمودية، يتقاطع المحور Y عند الصفر بشكل افتراضي،
// وهذا يعني أن الأعمدة لجميع القيم الموجودة أسفل الصفر تشير إلى القيم السلبية.
// يمكننا تعيين قيمة مختلفة لتقاطع المحور Y. في هذه الحالة، سنضبطها على 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### أنظر أيضا

* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
