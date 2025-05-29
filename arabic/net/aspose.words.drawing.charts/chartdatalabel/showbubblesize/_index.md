---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ShowBubbleSize مخططات الفقاعات لديك من خلال عرض أحجام تسميات البيانات. حسّن تمثيل بياناتك المرئي اليوم!
type: docs
weight: 130
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

يسمح بتحديد ما إذا كان سيتم عرض حجم الفقاعة لملصقات البيانات على الرسم البياني. ينطبق فقط على الرسوم البيانية الفقاعية. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowBubbleSize { get; set; }
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

* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
