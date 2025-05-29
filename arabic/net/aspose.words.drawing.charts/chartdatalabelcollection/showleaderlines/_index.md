---
title: ChartDataLabelCollection.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "عرض خطوط القادة" في ChartDataLabelCollection لتحسين تصورات بياناتك. تحكم بسهولة في خطوط القادة للحصول على رؤى أوضح!
type: docs
weight: 130
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

يسمح بتحديد ما إذا كان من الضروري عرض خطوط بادئة لملصقات البيانات لملصقات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## ملاحظات

ينطبق على المخططات الدائرية فقط. تنشئ الخطوط الرئيسية اتصالاً مرئيًا بين تسمية البيانات ونقطة البيانات المقابلة لها.

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) ملكية.

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
