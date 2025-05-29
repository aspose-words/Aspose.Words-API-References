---
title: OutlineOptions.HeadingsOutlineLevels
linktitle: HeadingsOutlineLevels
articleTitle: HeadingsOutlineLevels
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HeadingsOutlineLevels في OutlineOptions. تحكم في مستويات العناوين للمستندات المنظمة، وحسّن التنقل بسهولة.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

يحدد عدد مستويات العناوين (الفقرات المنسقة باستخدام أنماط العناوين) المراد تضمينها في مخطط المستند .

```csharp
public int HeadingsOutlineLevels { get; set; }
```

## ملاحظات

حدد 0 لعدم وجود عناوين في المخطط التفصيلي؛ وحدد 1 لمستوى واحد من العناوين في المخطط التفصيلي وهكذا.

الإعداد الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

## أمثلة

يوضح كيفية تحويل مستند كامل إلى PDF بثلاثة مستويات في مخطط المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج عناوين المستويات من 1 إلى 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "4" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان إدخال المخطط التفصيلي يحتوي على إدخالات لاحقة بمستوى أعلى بينها وبين الإدخال التالي من نفس المستوى أو المستوى الأدنى،
// سيظهر سهم على يسار المُدخلة. هذه المُدخلة هي "مالكة" العديد من هذه "المُدخلات الفرعية".
// في مستندنا، تعتبر إدخالات المخطط التفصيلي من مستوى العنوان الخامس إدخالات فرعية لإدخال المخطط التفصيلي الثاني من المستوى الرابع،
// إدخالات المستوى الرابع والخامس هي إدخالات فرعية للإدخال الثاني على المستوى الثالث، وهكذا.
// في المخطط التفصيلي، يمكننا النقر على سهم إدخال "المالك" لإخفاء/توسيع جميع إدخالاته الفرعية.
// اضبط خاصية "ExpandedOutlineLevels" على "2" لتوسيع جميع عناوين المستوى 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
// وانهيار جميع الإدخالات من المستوى 3 وما فوق عندما نفتح المستند.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### أنظر أيضا

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
