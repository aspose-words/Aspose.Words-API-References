---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words لـ .NET
description: ChartDataLabelCollection NumberFormat ملكية. يحصل علىChartNumberFormat مثيل يسمح بتعيين تنسيق الأرقام لتسميات البيانات الخاصة بسلسلة بأكملها في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

يحصل على[`ChartNumberFormat`](../../chartnumberformat/) مثيل يسمح بتعيين تنسيق الأرقام لتسميات البيانات الخاصة بسلسلة بأكملها.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## أمثلة

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
