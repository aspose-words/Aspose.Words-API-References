---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words لـ .NET
description: ChartAxis CrossesAt ملكية. يحدد مكان تقاطع المحور على المحور العمودي في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

يحدد مكان تقاطع المحور على المحور العمودي.

```csharp
public double CrossesAt { get; set; }
```

## ملاحظات

الخاصية لها تأثير فقط إذا[`Crosses`](../crosses/) تم ضبطها علىCustom. غير مدعوم من مخططات MS Office 2016 الجديدة.

يتم تحديد الوحدات حسب نوع المحور. عندما يكون المحور محور قيمة، تكون قيمة property رقمًا عشريًا على محور القيمة. عندما يكون المحور عبارة عن محور فئة زمنية، يتم تعريف القيمة كـ عدد صحيح من الأيام بالنسبة إلى التاريخ الأساسي (1899/12/30). بالنسبة لمحور فئة النص، تكون القيمة رقم فئة صحيحًا، يبدأ بـ 1 كفئة أولى.

## أمثلة

يوضح كيفية الحصول على محور الرسم البياني للعبور في موقع مخصص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// بالنسبة للمخططات العمودية، يتقاطع المحور Y عند الصفر افتراضيًا،
// مما يعني أن أعمدة جميع القيم الموجودة أسفل الصفر تشير إلى الأسفل لتمثل القيم السالبة.
// يمكننا تعيين قيمة مختلفة لعبور المحور ص. في هذه الحالة، سنضعه على 3.
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
