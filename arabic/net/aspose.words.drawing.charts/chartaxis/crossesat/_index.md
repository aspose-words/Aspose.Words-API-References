---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartAxis CrossesAt لتحديد نقاط التقاطع على المحور العمودي للرسم البياني بسهولة لتحسين تصور البيانات.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

يحدد مكان تقاطع المحور العمودي.

```csharp
public double CrossesAt { get; set; }
```

## ملاحظات

لا يكون للخاصية تأثير إلا إذا[`Crosses`](../crosses/) تم ضبطها علىCustom. غير مدعوم بواسطة المخططات الجديدة في MS Office 2016.

تُحدَّد الوحدات حسب نوع المحور. عندما يكون المحور محور قيمة، تكون قيمة الخاصية عددًا عشريًا على محور القيمة. عندما يكون المحور محور فئة زمنية، تُعرَّف القيمة على أنها ، وهو عدد صحيح من الأيام بالنسبة إلى تاريخ الأساس (30/12/1899). بالنسبة لمحور فئة نصية، تكون القيمة ، وهو عدد صحيح من الفئات، يبدأ بالرقم 1 كأول فئة.

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
