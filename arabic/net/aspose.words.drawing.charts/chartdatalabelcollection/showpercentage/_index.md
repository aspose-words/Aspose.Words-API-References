---
title: ChartDataLabelCollection.ShowPercentage
linktitle: ShowPercentage
articleTitle: ShowPercentage
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShowPercentage في ChartDataLabelCollection لتحسين مخططاتك الدائرية بعرض قيم النسب المئوية لعلامات البيانات. حسّن الوضوح والتحليل!
type: docs
weight: 150
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

يسمح بتحديد ما إذا كان سيتم عرض قيمة النسبة المئوية لملصقات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . ينطبق فقط على المخططات الدائرية.

```csharp
public bool ShowPercentage { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`ShowPercentage`](../../chartdatalabel/showpercentage/) الملكية.

## أمثلة

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// قم بإدراج سلسلة مخططات مخصصة مع اسم الفئة لكل قطاع، وجدول التردد الخاص بها.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// تمكين تسميات البيانات التي ستعرض النسبة المئوية والتردد لكل قطاع، وتعديل مظهرها.
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
