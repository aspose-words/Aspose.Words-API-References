---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى تنسيق الخط وتخصيصه لجميع تسميات بيانات السلسلة باستخدام خاصية الخط ChartDataLabelCollection لتحسين تصور البيانات.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

يوفر الوصول إلى تنسيق الخط الخاص بعلامات البيانات الخاصة بالسلسلة بأكملها.

```csharp
public Font Font { get; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`Font`](../../chartdatalabel/font/) الملكية.

## أمثلة

يوضح كيفية تمكين وتكوين تسميات البيانات لسلسلة الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف مخططًا خطيًا، ثم امسح سلسلة البيانات التجريبية الخاصة به للبدء بمخطط نظيف،
//ثم قم بتعيين عنوان.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// إدراج سلسلة مخططات مخصصة مع الأشهر كفئات للمحور X،
// والمبالغ العشرية المقابلة للمحور Y.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// قم بتمكين تسميات البيانات، ثم قم بتطبيق تنسيق رقم مخصص للقيم المعروضة في تسميات البيانات.
// سيعامل هذا التنسيق القيم العشرية المعروضة كملايين الدولارات الأمريكية.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### أنظر أيضا

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
