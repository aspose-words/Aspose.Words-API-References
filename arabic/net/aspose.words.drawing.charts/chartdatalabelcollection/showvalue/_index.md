---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ShowValue في ChartDataLabelCollection عرض بياناتك من خلال عرض قيم السلاسل. حسّن مخططاتك البيانية اليوم!
type: docs
weight: 170
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

يسمح بتحديد ما إذا كان سيتم عرض القيم في تسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowValue { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`ShowValue`](../../chartdatalabel/showvalue/) الملكية.

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
