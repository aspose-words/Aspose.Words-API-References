---
title: ChartAxis.Crosses
second_title: Aspose.Words لمراجع .NET API
description: ChartAxis ملكية. يحدد كيفية تقاطع هذا المحور مع المحور العمودي.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartaxis/crosses/
---
## ChartAxis.Crosses property

يحدد كيفية تقاطع هذا المحور مع المحور العمودي.

```csharp
public AxisCrosses Crosses { get; set; }
```

### ملاحظات

القيمة الافتراضية هيAutomatic.

الخاصية غير مدعومة بواسطة مخططات MS Office 2016 الجديدة.

### أمثلة

يوضح كيفية إدراج مخطط وتعديل مظهر محاوره.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة بيانات العرض التوضيحي للرسم البياني لتبدأ بمخطط نظيف.
chart.Series.Clear();

// أدخل سلسلة مخطط بفئات للمحور السيني والقيم الرقمية ذات الصلة للمحور ص.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// محاور المخطط لها خيارات متنوعة يمكن أن تغير مظهرها ،
// مثل اتجاههم ، وعلامات الوحدة الرئيسية / الثانوية ، وعلامات التجزئة.
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

* enum [AxisCrosses](../../axiscrosses/)
* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartaxis/)
* المجسم [Aspose.Words](../../../)


