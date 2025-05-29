---
title: ChartAxis.MajorUnit
linktitle: MajorUnit
articleTitle: MajorUnit
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartAxis MajorUnit لضبط المسافة بين علامات التجزئة الرئيسية بسهولة، مما يعزز تصور البيانات ووضوح الرسم البياني.
type: docs
weight: 130
url: /ar/net/aspose.words.drawing.charts/chartaxis/majorunit/
---
## ChartAxis.MajorUnit property

إرجاع أو تعيين المسافة بين علامات التجزئة الرئيسية.

```csharp
public double MajorUnit { get; set; }
```

## ملاحظات

النطاق الصحيح لقيمة أكبر من الصفر. تؤثر هذه الخاصية على محاور فئة الوقت وقيمة x000d_.

يؤدي تعيين هذه الخاصية إلى تعيين[`MajorUnitIsAuto`](../majorunitisauto/) الممتلكات إلى`خطأ شنيع`.

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
