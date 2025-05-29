---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الخط ChartDataLabel لتخصيص تنسيق خط ملصق البيانات الخاص بك بسهولة لتحسين الجاذبية البصرية والوضوح.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

يوفر الوصول إلى تنسيق الخط لملصق البيانات هذا.

```csharp
public Font Font { get; }
```

## أمثلة

يوضح كيفية استخدام التأثيرات ثلاثية الأبعاد مع المخططات الفقاعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// قم بتطبيق تسمية بيانات على كل فقاعة تعرض قطرها.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### أنظر أيضا

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
