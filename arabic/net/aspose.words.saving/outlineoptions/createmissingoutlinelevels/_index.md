---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية CreateMissingOutlineLevels في OutlineOptions على تعزيز تصدير المستندات من خلال إنشاء مستويات المخطط التفصيلي المفقودة تلقائيًا لتحسين التنظيم.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم إنشاء مستويات مخطط مفقودة أم لا عند تصدير المستند .

القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## أمثلة

يوضح كيفية العمل مع مستويات المخطط التفصيلي التي لا تحتوي على أي عناوين مقابلة عند حفظ مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج العناوين التي يمكن أن تكون بمثابة إدخالات جدول المحتويات للمستويين 1 و5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "5" لتضمين جميع عناوين المستويات 5 وما دونها في المخطط التفصيلي.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// تحتوي هذه الوثيقة على عناوين المستويات 1 و5، ولا تحتوي على عناوين المستويات 2 و3 و4.
// ستعامل وثيقة PDF الناتجة مستويات المخطط التفصيلي 2 و3 و4 على أنها "مفقودة".
// اضبط خاصية "CreateMissingOutlineLevels" على "true" لتضمين جميع المستويات المفقودة في المخطط التفصيلي،
// ترك إدخالات المخطط التفصيلي فارغة نظرًا لعدم وجود عناوين قابلة للاستخدام.
// اضبط خاصية "CreateMissingOutlineLevels" على "false" لتجاهل مستويات المخطط التفصيلي المفقودة،
// وتعامل مع عناوين المستوى الخامس على أنها عناوين المستوى الثاني.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### أنظر أيضا

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
