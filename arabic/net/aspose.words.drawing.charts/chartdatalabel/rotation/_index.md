---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تدوير علامات بيانات المخطط لتخصيص زوايا العلامات بسهولة في مخططاتك. حسّن تصور البيانات بتحكم دقيق!
type: docs
weight: 110
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

يحصل على أو يضبط دوران الملصق بالدرجات.

```csharp
public int Rotation { get; set; }
```

## ملاحظات

يتراوح نطاق القيم المقبولة بين -١٨٠ و١٨٠ شاملةً. القيمة الافتراضية هي ٠.

إذا كان[`Orientation`](../orientation/) القيمة هيHorizontalشكل الملصق x000d_، إن وُجد، يُدوّر مع نص الملصق. وإلا، يُدوّر نص الملصق فقط. x000d_

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

* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
