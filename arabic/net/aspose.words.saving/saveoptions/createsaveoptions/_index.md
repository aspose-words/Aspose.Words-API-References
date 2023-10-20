---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words لـ .NET
description: SaveOptions CreateSaveOptions طريقة. إنشاء كائن خيارات الحفظ من فئة مناسبة لتنسيق الحفظ المحدد في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

إنشاء كائن خيارات الحفظ من فئة مناسبة لتنسيق الحفظ المحدد.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | تنسيق الحفظ الذي سيتم إنشاء كائن خيارات الحفظ له. |

### قيمة الإرجاع

كائن من فئة مشتقة من[`SaveOptions`](../).

## أمثلة

يعرض خيارًا لتحسين استهلاك الذاكرة عند تحويل مستندات كبيرة إلى PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// اضبط خاصية "تحسين الذاكرة" على "صحيح" لتقليل مساحة الذاكرة لعمليات حفظ المستندات الكبيرة
// على حساب زيادة مدة العملية.
// اضبط خاصية "تحسين الذاكرة" على "خطأ" لحفظ المستند كملف PDF بشكل طبيعي.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

إنشاء كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المحدد.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | يحدد ملحق اسم الملف هذا فئة كائن خيارات الحفظ المراد إنشاؤه. |

### قيمة الإرجاع

كائن من فئة مشتقة من[`SaveOptions`](../).

## أمثلة

يوضح كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.

```csharp
Document doc = new Document();

// تمكين التحديث التلقائي للنمط، ولكن لا ترفق مستند القالب.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// نظرًا لعدم وجود مستند قالب، لم يكن للمستند مكان لتتبع تغييرات النمط.
// استخدم كائن SaveOptions لتعيين القالب تلقائيًا
// إذا كانت الوثيقة التي نقوم بحفظها لا تحتوي على واحدة.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
