---
title: ChartDataLabelCollection.ShowPercentage
linktitle: ShowPercentage
articleTitle: ShowPercentage
second_title: Aspose.Words لـ .NET
description: ChartDataLabelCollection ShowPercentage ملكية. يسمح بتحديد ما إذا كان سيتم عرض قيمة النسبة المئوية لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هيخطأ شنيع . ينطبق فقط على المخططات الدائرية في C#.
type: docs
weight: 120
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

يسمح بتحديد ما إذا كان سيتم عرض قيمة النسبة المئوية لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . ينطبق فقط على المخططات الدائرية.

```csharp
public bool ShowPercentage { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لتسمية بيانات فردية باستخدام [`ShowPercentage`](../../chartdatalabel/showpercentage/) الملكية.

## أمثلة

يوضح كيفية التعامل مع تسميات البيانات الخاصة بالمخطط الدائري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أدخل سلسلة مخططات مخصصة مع اسم فئة لكل قطاع وجدول تكرارها.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// تمكين تسميات البيانات التي ستعرض النسبة المئوية والتكرار لكل قطاع، وتعديل مظهرها.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### أنظر أيضا

* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
