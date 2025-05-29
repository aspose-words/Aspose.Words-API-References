---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.AxisTickLabels، المصممة لتعزيز علامات محور الرسم البياني الخاص بك باستخدام خصائص قابلة للتخصيص لتحسين تصور البيانات.
type: docs
weight: 840
url: /ar/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

يمثل خصائص علامات المحور.

```csharp
public class AxisTickLabels
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | يحصل على محاذاة النص لعلامات محور العلامة أو يعينها. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | يوفر إمكانية الوصول إلى تنسيق الخط الخاص بعلامات التجزئة. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كان سيتم استخدام الفاصل الزمني التلقائي لرسم تسميات العلامات. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | يحصل على أو يعين مسافة علامات التجزئة من المحور. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | يحصل على اتجاه نص علامة التجزئة أو يعينه. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | يحصل على موضع علامات التجزئة على المحور أو يعينه. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | يحصل على أو يضبط دوران علامات التجزئة بالدرجات. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | يحصل على الفاصل الزمني الذي يتم فيه رسم تسميات العلامات أو يعينه. |

## أمثلة

يوضح كيفية إدراج مخطط وتعديل مظهر محاوره.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// قم بإدراج سلسلة مخططات تحتوي على فئات لمحور X والقيم الرقمية المقابلة لمحور Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// تحتوي محاور الرسم البياني على خيارات مختلفة يمكنها تغيير مظهرها،
// مثل اتجاهها، وعلامات الوحدة الرئيسية/الثانوية، وعلامات التجزئة.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// لا تحتوي المخططات العمودية على محور Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
