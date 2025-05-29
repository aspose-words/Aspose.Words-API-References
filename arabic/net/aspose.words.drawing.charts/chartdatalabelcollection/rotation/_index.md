---
title: ChartDataLabelCollection.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words لـ .NET
description: اضبط دوران مجموعة علامات بيانات المخطط (ChartDataLabelCollection) لتحسين وضوحها. خصص زوايا علامات البيانات لتحسين سهولة قراءة مخططك وتأثيره.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/rotation/
---
## ChartDataLabelCollection.Rotation property

يحصل على أو يعين دوران تسميات البيانات للسلسلة بأكملها بالدرجات.

```csharp
public int Rotation { get; set; }
```

## ملاحظات

يتراوح نطاق القيم المقبولة بين -١٨٠ و١٨٠ شاملةً. القيمة الافتراضية هي ٠.

إذا كان[`Orientation`](../orientation/) القيمة هيHorizontalأشكال التسمية، إن وجدت، تُدوّر مع نص التسمية. وإلا، يُدوّر نص التسمية فقط.

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

* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
