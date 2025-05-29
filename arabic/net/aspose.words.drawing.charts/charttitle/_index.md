---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartTitle لإدارة عناوين المخططات وتخصيصها بسهولة لتحسين تصور البيانات.
type: docs
weight: 1140
url: /ar/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

يوفر الوصول إلى خصائص عنوان الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع المخططات](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartTitle
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | يوفر الوصول إلى تنسيق الخط لعنوان الرسم البياني. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | يوفر إمكانية الوصول إلى تنسيق التعبئة والخط لعنوان الرسم البياني. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | يحدد ما إذا كان سيتم السماح لعناصر الرسم البياني الأخرى بالتداخل مع العنوان. بشكل افتراضي، يكون التراكب هو`خطأ شنيع` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | يحدد ما إذا كان سيتم عرض العنوان لهذا الرسم البياني. القيمة الافتراضية هي`حقيقي` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | يحصل على نص عنوان الرسم البياني أو يعينه. إذا`باطل` أو إذا تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا. |

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
