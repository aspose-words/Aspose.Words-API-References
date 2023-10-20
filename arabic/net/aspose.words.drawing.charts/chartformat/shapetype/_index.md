---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words لـ .NET
description: ChartFormat ShapeType ملكية. الحصول على أو تعيين نوع الشكل لعنصر المخطط الأصلي في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

الحصول على أو تعيين نوع الشكل لعنصر المخطط الأصلي.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## ملاحظات

حاليًا، لا يمكن استخدام الخاصية إلا لتسميات البيانات.

## أمثلة

يوضح كيفية تعيين تنسيق التعبئة والحد ووسيلة الشرح لتسميات بيانات المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// حذف السلسلة الافتراضية التي تم إنشاؤها.
chart.Series.Clear();

// إضافة سلسلة جديدة.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// إظهار تسميات البيانات.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// تنسيق تسميات البيانات كوسيلة شرح.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// تغيير التعبئة والحدود لتسمية البيانات الفردية.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### أنظر أيضا

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
