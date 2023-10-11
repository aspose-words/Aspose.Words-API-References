---
title: ChartAxis.TickMarkSpacing
second_title: Aspose.Words لمراجع .NET API
description: ChartAxis ملكية. الحصول على أو تعيين الفاصل الزمني الذي يتم عنده رسم علامات التجزئة.
type: docs
weight: 270
url: /ar/net/aspose.words.drawing.charts/chartaxis/tickmarkspacing/
---
## ChartAxis.TickMarkSpacing property

الحصول على أو تعيين الفاصل الزمني الذي يتم عنده رسم علامات التجزئة.

```csharp
public int TickMarkSpacing { get; set; }
```

### ملاحظات

الخاصية لها تأثير على فئة النص ومحاور السلسلة. وهو غير مدعوم من قبل مخططات MS Office 2016 الجديدة.

النطاق الصالح للقيمة أكبر من أو يساوي 1.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartaxis/)
* المجسم [Aspose.Words](../../../)


