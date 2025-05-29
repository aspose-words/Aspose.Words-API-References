---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية ضبط خاصية SecondSectionSize في ChartSeriesGroup لتخصيص حجم القسم الثانوي لمخطط الفطيرة الخاص بك بشكل فعال.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

يحصل على حجم القسم الثانوي للمخطط الدائري أو يعينه كنسبة مئوية.

```csharp
public int SecondSectionSize { get; set; }
```

## ملاحظات

ينطبق على مجموعات السلسلةPieOfPie و PieOfBar أنواع.

يتراوح نطاق القيم المقبولة بين 5 و200. القيمة الافتراضية هي 75.

## أمثلة

يوضح كيفية إنشاء مخطط دائري وتنسيقه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

//تنسيق مخطط الفطيرة.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### أنظر أيضا

* class [ChartSeriesGroup](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
