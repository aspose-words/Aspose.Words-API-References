---
title: ChartDataLabelCollection.Font
second_title: Aspose.Words لمراجع .NET API
description: ChartDataLabelCollection ملكية. يوفر الوصول إلى تنسيق الخط الخاص بتسميات البيانات الخاصة بالسلسلة بأكملها.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

يوفر الوصول إلى تنسيق الخط الخاص بتسميات البيانات الخاصة بالسلسلة بأكملها.

```csharp
public Font Font { get; }
```

### ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لتسمية بيانات فردية باستخدام [`Font`](../../chartdatalabel/font/) الملكية.

### أمثلة

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

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* المجسم [Aspose.Words](../../../)


