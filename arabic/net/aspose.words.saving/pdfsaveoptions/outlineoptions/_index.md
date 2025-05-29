---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OutlineOptions في PdfSaveOptions لتخصيص مخططات ملفات PDF بسهولة. حسّن تجربة تصفحك وحسّن استخدام مستنداتك!
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

يمكن إنشاء المخططات التفصيلية من العناوين والإشارات المرجعية.

بالنسبة للعناوين، يتم تحديد مستوى المخطط حسب مستوى العنوان.

من الممكن تحديد الحد الأقصى لمستوى العنوان المراد تضمينه في المخططات التفصيلية أو تعطيل مخططات العنوان على الإطلاق.

بالنسبة لإشارات المرجعية، يمكن تعيين مستوى المخطط التفصيلي في الخيارات كقيمة افتراضية لجميع الإشارات المرجعية أو كقيم فردية لإشارات مرجعية معينة.

كما يمكن تصدير المخططات التفصيلية إلى تنسيق XPS باستخدام نفس`OutlineOptions` فصل.

## أمثلة

يوضح كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند PDF المحفوظ.

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

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "2" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 2 من المخطط التفصيلي.
// لن يظهر آخر عنوانين قمنا بإدخالهما أعلاه.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

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

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
