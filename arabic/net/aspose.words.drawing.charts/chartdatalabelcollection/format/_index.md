---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تنسيق ChartDataLabelCollection للوصول بسهولة إلى تنسيق التعبئة والخطوط القابل للتخصيص لعناوين بياناتك. حسّن مخططاتك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

يوفر إمكانية الوصول إلى تنسيق التعبئة والخطوط لملصقات البيانات.

```csharp
public ChartFormat Format { get; }
```

## أمثلة

يوضح كيفية تعيين تنسيق التعبئة والحدود والتعليق التوضيحي لملصقات بيانات الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//إضافة سلسلة جديدة.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

//إظهار تسميات البيانات.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

//تنسيق تسميات البيانات على شكل نصوص توضيحية.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// تغيير التعبئة والحدود لعلامة بيانات فردية.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### أنظر أيضا

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
