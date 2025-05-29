---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartDataLabelCollection NumberFormat لتخصيص تنسيقات تسميات البيانات بسهولة لسلسلتك بأكملها، مما يعزز الوضوح والعرض.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

يحصل على[`ChartNumberFormat`](../../chartnumberformat/) مثال يسمح بتعيين تنسيق الأرقام لملصقات البيانات الخاصة بالسلسلة بأكملها.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
