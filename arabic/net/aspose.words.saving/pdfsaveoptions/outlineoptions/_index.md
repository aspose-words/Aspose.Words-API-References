---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions OutlineOptions ملكية. يسمح بتحديد خيارات المخطط التفصيلي في C#.
type: docs
weight: 240
url: /ar/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

يسمح بتحديد خيارات المخطط التفصيلي.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## ملاحظات

يمكن إنشاء الخطوط العريضة من العناوين والإشارات المرجعية.

بالنسبة للعناوين، يتم تحديد مستوى المخطط التفصيلي حسب مستوى العنوان.

من الممكن ضبط الحد الأقصى لمستوى العنوان ليتم تضمينه في الخطوط العريضة أو تعطيل الخطوط العريضة للعناوين على الإطلاق.

بالنسبة لمستوى المخطط التفصيلي للإشارات المرجعية، يمكن تعيينه في الخيارات كقيمة افتراضية لجميع الإشارات المرجعية أو كقيم فردية لإشارات مرجعية معينة.

كما يمكن تصدير المخططات التفصيلية إلى تنسيق XPS باستخدام نفس التنسيق`OutlineOptions` فصل.

## أمثلة

يوضح كيفية تحديد مستوى العناوين التي ستظهر في المخطط التفصيلي لمستند PDF محفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل العناوين التي يمكن أن تكون بمثابة إدخالات جدول المحتويات للمستويات 1، 2، ثم 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "2" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 2 من المخطط التفصيلي.
// لن يظهر العنوانان الأخيران اللذان أدخلناهما أعلاه.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

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

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
