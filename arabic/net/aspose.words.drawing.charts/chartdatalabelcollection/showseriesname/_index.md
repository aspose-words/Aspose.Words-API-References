---
title: ChartDataLabelCollection.ShowSeriesName
second_title: Aspose.Words لمراجع .NET API
description: ChartDataLabelCollection ملكية. إرجاع قيمة منطقية أو تعيينها للإشارة إلى سلوك عرض اسم السلسلة لتسميات البيانات الخاصة بالسلسلة بأكملها. حقيقي لإظهار اسم المسلسلخطأ شنيع لإخفاء. بشكل افتراضيخطأ شنيع .
type: docs
weight: 130
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

إرجاع قيمة منطقية أو تعيينها للإشارة إلى سلوك عرض اسم السلسلة لتسميات البيانات الخاصة بالسلسلة بأكملها. `حقيقي` لإظهار اسم المسلسل؛`خطأ شنيع` لإخفاء. بشكل افتراضي`خطأ شنيع` .

```csharp
public bool ShowSeriesName { get; set; }
```

### ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لتسمية بيانات فردية باستخدام [`ShowSeriesName`](../../chartdatalabel/showseriesname/) الملكية.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* المجسم [Aspose.Words](../../../)


