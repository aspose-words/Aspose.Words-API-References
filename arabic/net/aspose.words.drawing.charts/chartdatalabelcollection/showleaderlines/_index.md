---
title: ChartDataLabelCollection.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: Aspose.Words لـ .NET
description: ChartDataLabelCollection ShowLeaderLines ملكية. يسمح بتحديد ما إذا كان من الضروري إظهار الخطوط الرئيسية لتسمية البيانات لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

يسمح بتحديد ما إذا كان من الضروري إظهار الخطوط الرئيسية لتسمية البيانات لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## ملاحظات

ينطبق على المخططات الدائرية فقط. تُنشئ الخطوط الرئيسية اتصالاً مرئيًا بين تسمية البيانات ونقطة البيانات المقابلة لها.

يمكن تجاوز القيمة المحددة لهذه الخاصية لتسمية بيانات فردية باستخدام [`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) ملكية.

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
