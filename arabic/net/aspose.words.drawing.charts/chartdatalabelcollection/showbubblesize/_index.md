---
title: ChartDataLabelCollection.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ShowBubbleSize في ChartDataLabelCollection مخططات الفقاعات لديك من خلال التحكم في رؤية تسميات البيانات. حسّن عرض بياناتك!
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/
---
## ChartDataLabelCollection.ShowBubbleSize property

يسمح بتحديد ما إذا كان سيتم عرض حجم الفقاعة لملصقات البيانات الخاصة بالسلسلة بأكملها. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowBubbleSize { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`ShowBubbleSize`](../../chartdatalabel/showbubblesize/) الملكية.

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
