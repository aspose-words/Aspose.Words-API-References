---
title: ChartTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: خصّص عنوان مخططك بسهولة! عيّن أو احصل على خاصية "نص عنوان المخطط" لإضفاء لمسة شخصية. أنشئ العناوين تلقائيًا عند الحاجة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

يحصل على نص عنوان الرسم البياني أو يعينه. إذا`باطل` أو إذا تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا.

```csharp
public string Text { get; set; }
```

## ملاحظات

يستخدم[`Show`](../show/) الخيار إذا كنت بحاجة إلى إخفاء العنوان.

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
