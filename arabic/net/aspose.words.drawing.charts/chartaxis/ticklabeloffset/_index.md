---
title: ChartAxis.TickLabelOffset
linktitle: TickLabelOffset
articleTitle: TickLabelOffset
second_title: Aspose.Words لـ .NET
description: ChartAxis TickLabelOffset ملكية. الحصول على أو تعيين مسافة التسميات من المحور في C#.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing.charts/chartaxis/ticklabeloffset/
---
## ChartAxis.TickLabelOffset property

الحصول على أو تعيين مسافة التسميات من المحور.

```csharp
public int TickLabelOffset { get; set; }
```

## ملاحظات

تمثل الخاصية نسبة مئوية من إزاحة التسمية الافتراضية.

النطاق الصالح هو من 0 إلى 1000 بالمائة ضمناً. القيمة الافتراضية هي 100%.

الخاصية لها تأثير فقط على محاور الفئة. وهو غير مدعوم بالمخططات الجديدة لـ MS Office 2016.

## أمثلة

يوضح كيفية إدراج مخطط وتعديل مظهر محاوره.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// قم بإدراج سلسلة مخططات تحتوي على فئات للمحور X والقيم الرقمية المعنية للمحور Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// تحتوي محاور المخطط على خيارات متعددة يمكنها تغيير مظهرها،
// مثل اتجاهها، وعلامات التجزئة للوحدة الرئيسية/الثانوية، وعلامات التجزئة.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// لا تحتوي المخططات العمودية على محور Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### أنظر أيضا

* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
