---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words لـ .NET
description: ChartNumberFormat FormatCode ملكية. الحصول على رمز التنسيق المطبق على تسمية البيانات أو تعيينه في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

الحصول على رمز التنسيق المطبق على تسمية البيانات أو تعيينه.

```csharp
public string FormatCode { get; set; }
```

## ملاحظات

يتم استخدام تنسيق الأرقام لتغيير الطريقة التي تظهر بها القيمة في تسمية البيانات ويمكن استخدامه ببعض الطرق الإبداعية للغاية. أمثلة تنسيقات الأرقام:

الرقم - "#،##0.00"

العملة - "\"$\"#,##0.00"

الوقت - "[$-x-systime]h:mm:ss AM/PM"

التاريخ - "اليوم/الشهر/السنة"

النسبة المئوية - "0.00%"

جزء - "# ؟/؟"

علمي - "0.00E+00"

نص - "@"

المحاسبة - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_ -;_-@_-"

مخصص مع اللون - "[أحمر]-#،##0.0"

## أمثلة

يوضح كيفية تعيين التنسيق لقيم المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة إلى المخطط مع فئات المحور السيني،
 // وقيم رقمية كبيرة خاصة بالمحور Y.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // قم بتعيين تنسيق الأرقام لتسميات تحديد المحور Y بحيث لا يتم تجميع الأرقام بفواصل.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// يمكن لهذه العلامة تجاوز القيمة المذكورة أعلاه ورسم تنسيق الأرقام من الخلية المصدر.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

يوضح كيفية تمكين تسميات البيانات وتكوينها لسلسلة مخططات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف مخططًا خطيًا، ثم امسح سلسلة بيانات العرض التوضيحي الخاصة به للبدء بمخطط نظيف،
// ثم قم بتعيين العنوان.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// قم بإدراج سلسلة مخططات مخصصة بالأشهر كفئات للمحور السيني،
// والمبالغ العشرية المعنية للمحور ص.
ChartSeries series = chart.Series.Add("Revenue", 
    new[] { "January", "February", "March" }, 
    new[] { 25.611d, 21.439d, 33.750d });

// قم بتمكين تسميات البيانات، ثم قم بتطبيق تنسيق أرقام مخصص للقيم المعروضة في تسميات البيانات.
// سيتعامل هذا التنسيق مع القيم العشرية المعروضة كملايين الدولارات الأمريكية.
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
