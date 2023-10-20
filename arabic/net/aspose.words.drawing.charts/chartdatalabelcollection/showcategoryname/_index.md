---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: Aspose.Words لـ .NET
description: ChartDataLabelCollection ShowCategoryName ملكية. يسمح بتحديد ما إذا كان سيتم عرض اسم الفئة لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

يسمح بتحديد ما إذا كان سيتم عرض اسم الفئة لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowCategoryName { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لتسمية بيانات فردية باستخدام [`ShowCategoryName`](../../chartdatalabel/showcategoryname/) الملكية.

## أمثلة

يوضح كيفية التعامل مع تسميات البيانات الخاصة بالمخطط الفقاعي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة بإحداثيات X/Y وقطر كل من الفقاعات.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// قم بتمكين تسميات البيانات، ثم قم بتعديل مظهرها.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

### أنظر أيضا

* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
