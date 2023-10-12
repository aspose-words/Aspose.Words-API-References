---
title: OutlineOptions.CreateMissingOutlineLevels
second_title: Aspose.Words لمراجع .NET API
description: OutlineOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم إنشاء مستويات مخطط تفصيلي مفقودة أم لا عندما يتم تصدير المستند .
type: docs
weight: 30
url: /ar/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم إنشاء مستويات مخطط تفصيلي مفقودة أم لا عندما يتم تصدير المستند .

القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

### أمثلة

يوضح كيفية العمل مع مستويات المخطط التفصيلي التي لا تحتوي على أي عناوين مقابلة عند حفظ مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل العناوين التي يمكن أن تكون بمثابة إدخالات جدول المحتويات للمستويات 1 و5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "5" لتضمين جميع عناوين المستويات 5 وما دونها في المخطط التفصيلي.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// تحتوي هذه الوثيقة على عناوين المستويات 1 و5، ولا تحتوي على عناوين المستويات 2 و3 و4.
// سوف يتعامل مستند PDF الناتج مع مستويات المخطط التفصيلي 2 و3 و4 على أنها "مفقودة".
// قم بتعيين الخاصية "CreateMissingOutlineLevels" على "true" لتضمين جميع المستويات المفقودة في المخطط التفصيلي،
// ترك إدخالات المخطط التفصيلي فارغة نظرًا لعدم وجود عناوين قابلة للاستخدام.
// اضبط الخاصية "CreateMissingOutlineLevels" على "خطأ" لتجاهل مستويات المخطط التفصيلي المفقودة،
// وتعامل مع عناوين المستوى 5 للمخطط التفصيلي على أنها المستوى 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### أنظر أيضا

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../outlineoptions/)
* المجسم [Aspose.Words](../../../)


