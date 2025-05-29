---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartDataTable لتخصيص جداول بيانات المخططات بسهولة وتعزيز تصور البيانات لديك باستخدام ميزات قوية.
type: docs
weight: 990
url: /ar/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

يسمح بتحديد خصائص جدول بيانات الرسم البياني.

```csharp
public class ChartDataTable
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | يوفر الوصول إلى تنسيق الخط لجدول البيانات. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | يوفر إمكانية الوصول إلى تعبئة خلفية النص وتنسيق الحدود لجدول البيانات. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كان سيتم عرض حد أفقي لجدول البيانات. القيمة الافتراضية هي`حقيقي` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات. القيمة الافتراضية هي`حقيقي` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كان سيتم عرض حدود تفصيلية، أي حدود حول أسماء السلسلة والفئة، . القيمة الافتراضية هي`حقيقي` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كان سيتم عرض حد عمودي لجدول البيانات. القيمة الافتراضية هي`حقيقي` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | يحصل على علامة أو يعينها للإشارة إلى ما إذا كان سيتم عرض جدول البيانات للرسم البياني. القيمة الافتراضية هي`خطأ شنيع` . |

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
