---
title: ChartAxis.TickMarkSpacing
linktitle: TickMarkSpacing
articleTitle: TickMarkSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartAxis TickMarkSpacing لتخصيص فترات علامات التجزئة، مما يعزز قابلية قراءة الرسم البياني وجاذبيته البصرية.
type: docs
weight: 240
url: /ar/net/aspose.words.drawing.charts/chartaxis/tickmarkspacing/
---
## ChartAxis.TickMarkSpacing property

يحصل على الفاصل الزمني الذي يتم فيه رسم علامات التجزئة أو يعينه.

```csharp
public int TickMarkSpacing { get; set; }
```

## ملاحظات

هذه الخاصية تؤثر على محاور فئات النصوص والسلاسل. لا يدعمها MS Office 2016 new charts.

النطاق الصحيح للقيمة أكبر من أو يساوي 1.

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

* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
