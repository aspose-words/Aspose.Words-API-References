---
title: ChartTitle.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تراكب عنوان المخطط، وتداخل عناصر التحكم لعرض مرئي أوضح. حسّن مخططاتك بسهولة مع هذا الإعداد البسيط!
type: docs
weight: 30
url: /ar/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

يحدد ما إذا كان سيتم السماح لعناصر الرسم البياني الأخرى بالتداخل مع العنوان. بشكل افتراضي، يكون التراكب هو`خطأ شنيع` .

```csharp
public bool Overlay { get; set; }
```

## أمثلة

يوضح كيفية إدراج مخطط وتعيين عنوان.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل مخطط باستخدام منشئ المستندات واحصل على مخططه.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

//استخدم خاصية "العنوان" لإعطاء عنوان لمخططنا، والذي يظهر في الجزء العلوي الأوسط من منطقة المخطط.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // قم بضبط خاصية "إظهار" على "صحيح" لجعل العنوان مرئيًا.
title.Show = true;

// اضبط خاصية "Overlay" على "true" امنح عناصر الرسم البياني الأخرى مساحة أكبر من خلال السماح لها بالتداخل مع العنوان
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### أنظر أيضا

* class [ChartTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
