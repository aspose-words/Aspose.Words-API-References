---
title: ChartAxis.TickLabelSpacingIsAuto
linktitle: TickLabelSpacingIsAuto
articleTitle: TickLabelSpacingIsAuto
second_title: Aspose.Words لـ .NET
description: ChartAxis TickLabelSpacingIsAuto ملكية. الحصول على أو تعيين علامة تشير إلى ما إذا كان سيتم استخدام الفاصل الزمني التلقائي لرسم تسميات التجزئة في C#.
type: docs
weight: 260
url: /ar/net/aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/
---
## ChartAxis.TickLabelSpacingIsAuto property

الحصول على أو تعيين علامة تشير إلى ما إذا كان سيتم استخدام الفاصل الزمني التلقائي لرسم تسميات التجزئة.

```csharp
public bool TickLabelSpacingIsAuto { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي`.

الخاصية لها تأثير على فئة النص ومحاور السلسلة. وهو غير مدعوم من قبل مخططات MS Office 2016 الجديدة.

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
