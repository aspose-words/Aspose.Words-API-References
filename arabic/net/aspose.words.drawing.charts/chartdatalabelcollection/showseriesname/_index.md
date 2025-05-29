---
title: ChartDataLabelCollection.ShowSeriesName
linktitle: ShowSeriesName
articleTitle: ShowSeriesName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShowSeriesName في ChartDataLabelCollection، وتحكّم بسهولة في ظهور أسماء السلاسل في تسميات بياناتك. حسّن مخططاتك اليوم!
type: docs
weight: 160
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

يعيد أو يعين قيمة منطقية للإشارة إلى سلوك عرض اسم السلسلة لملصقات البيانات الخاصة بالسلسلة بأكملها. `حقيقي` لإظهار اسم السلسلة؛`خطأ شنيع` للإخفاء. افتراضيًا`خطأ شنيع` .

```csharp
public bool ShowSeriesName { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`ShowSeriesName`](../../chartdatalabel/showseriesname/) الملكية.

## أمثلة

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

 // أضف سلسلة مخصصة مع إحداثيات X/Y وقطر كل فقاعة.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// تمكين تسميات البيانات، ثم تعديل مظهرها.
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
