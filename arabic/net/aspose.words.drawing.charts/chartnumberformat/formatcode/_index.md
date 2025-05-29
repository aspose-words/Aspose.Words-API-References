---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية ChartNumberFormat FormatCode لتخصيص تنسيقات تسميات البيانات للحصول على رؤى أكثر وضوحًا وعرض محسّن للبيانات.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

يحصل على رمز التنسيق المطبق على تسمية البيانات أو يعينه.

```csharp
public string FormatCode { get; set; }
```

## ملاحظات

يتم استخدام تنسيق الأرقام لتغيير طريقة ظهور القيمة في تسمية البيانات ويمكن استخدامه بطرق مبتكرة للغاية. أمثلة على تنسيقات الأرقام:

الرقم - "#,##0.00"

العملة - "\"$\"#,##0.00"

الوقت - "[$-x-systime]h:mm:ss AM/PM"

التاريخ - "د/ش/س"

النسبة المئوية - "0.00%"

جزء - "# ؟/؟"

علمي - "0.00E+00"

نص - "@"

المحاسبة - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

مخصص باللون - "[أحمر]-#,##0.0"

## أمثلة

يوضح كيفية تعيين التنسيق لقيم الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة إلى الرسم البياني مع فئات للمحور X،
 // والقيم الرقمية الكبيرة المقابلة للمحور Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // قم بتعيين تنسيق الأرقام لعناوين علامات المحور Y لعدم تجميع الأرقام بفاصلات.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// يمكن لهذا العلم تجاوز القيمة أعلاه ورسم تنسيق الرقم من الخلية المصدر.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

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

* class [ChartNumberFormat](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
