---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Position في ChartDataLabelCollection لتخصيص مواضع تسميات البيانات بسهولة لتحسين تصور البيانات ووضوحها.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

يحصل على موضع تسميات البيانات أو يعينه.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## ملاحظات

يمكن تعيين الموضع لملصقات البيانات لأنواع سلسلة المخططات التالية:

-Bar ،Column ، Histogram ،Pareto ، Waterfall القيم المسموح بها:Center ، InsideBase ،InsideEnd و OutsideEnd؛

-BarStacked ،BarPercentStacked ، ColumnStacked ،ColumnPercentStacked ;القيم المسموح بها :Center ،InsideBase وInsideEnd؛

-Bubble ،Bubble3D ، Line ،LineStacked ، LinePercentStacked ،Scatter ، Stock القيم المسموح بها:Center ، Left ،Right ، Above وBelow؛

-Pie ،Pie3D ، PieOfBar ،PieOfPie القيم المسموح بها: Center ،InsideEnd ، OutsideEnd وBestFit؛

-BoxAndWhisker القيم المسموح بها: Left ،Right ، Above وBelow.

## أمثلة

يوضح كيفية تعيين موضع تسمية البيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مخطط عمودي.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

//حذف السلسلة المولدة افتراضيًا.
seriesColl.Clear();

//إضافة سلسلة.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// إظهار تسميات البيانات وتعيين لون الخط.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// تعيين موضع تسمية البيانات.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### أنظر أيضا

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
