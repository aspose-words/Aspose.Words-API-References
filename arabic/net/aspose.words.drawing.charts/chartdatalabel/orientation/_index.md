---
title: ChartDataLabel.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اتجاه ChartDataLabel لتخصيص اتجاه نص التسمية بسهولة لتحسين تصور البيانات ووضوحها في مخططاتك.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/orientation/
---
## ChartDataLabel.Orientation property

يحصل على اتجاه نص الملصق أو يعينه.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## ملاحظات

القيمة الافتراضية هيHorizontal .

## أمثلة

يوضح كيفية تغيير الاتجاه والدوران لملصقات البيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

//إظهار تسميات البيانات.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// قم بتحديد شكل تسمية البيانات.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// تعيين اتجاه تسمية البيانات وتدويرها للسلسلة بأكملها.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// تغيير الاتجاه والدوران لعلامة البيانات الأولى.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### أنظر أيضا

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
