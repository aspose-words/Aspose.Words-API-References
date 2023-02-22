---
title: ChartSeries.Format
second_title: Aspose.Words لمراجع .NET API
description: ChartSeries ملكية. يوفر الوصول لتعبئة وتنسيق خط السلسلة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

يوفر الوصول لتعبئة وتنسيق خط السلسلة.

```csharp
public ChartFormat Format { get; }
```

### أمثلة

يبذر كيفية تعيين لون السلسلة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// حذف السلسلة الافتراضية التي تم إنشاؤها.
seriesColl.Clear();

// إنشاء مصفوفة أسماء الفئات.
string[] categories = new[] { "Category 1", "Category 2" };

// إضافة سلسلة جديدة. يجب أن تكون صفائف القيمة والفئات بنفس الحجم.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// تعيين لون السلسلة.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### أنظر أيضا

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartseries/)
* المجسم [Aspose.Words](../../../)


