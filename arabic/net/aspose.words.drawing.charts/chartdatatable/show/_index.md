---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words لـ .NET
description: تحكم في عرض مخططك باستخدام خاصية "عرض جدول بيانات المخطط". يمكنك تبديل عرض جدول البيانات بسهولة لتحسين رؤى البيانات. الافتراضي خطأ.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

يحصل على علامة أو يعينها للإشارة إلى ما إذا كان سيتم عرض جدول البيانات للرسم البياني. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool Show { get; set; }
```

## ملاحظات

لا تدعم أنواع المخططات التالية جداول البيانات: مخطط التشتت، المخطط الدائري، المخطط الدائري الدائري، المخطط السطحي، المخطط الراداري، مخطط الشجرة، مخطط أشعة الشمس، المخطط التكراري، مخطط باريتو، مخطط الصندوق والشارب، مخطط الشلال، المخطط القمعي، المخطط المركب الذي يتضمن سلسلة من هذه الأنواع. يؤدي عرض جدول بيانات لأنواع المخططات إلى ظهور خطأ.InvalidOperationException استثناء .

## أمثلة

يوضح كيفية عرض جدول البيانات باستخدام بيانات سلسلة الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### أنظر أيضا

* class [ChartDataTable](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
