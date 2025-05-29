---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CreateSaveOptions لإنشاء خيارات حفظ مخصصة للتنسيق المفضل لديك بسهولة، مما يعزز كفاءة إدارة المستندات لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

ينشئ كائن خيارات الحفظ لفئة مناسبة لتنسيق الحفظ المحدد.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | تنسيق الحفظ الذي سيتم إنشاء كائن خيارات الحفظ له. |

### قيمة الإرجاع

كائن من فئة مشتق من[`SaveOptions`](../).

## أمثلة

يُظهر خيارًا لتحسين استهلاك الذاكرة عند تحويل المستندات الكبيرة إلى PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// اضبط خاصية "MemoryOptimization" على "true" لتقليل حجم الذاكرة لعمليات حفظ المستندات الكبيرة
// على حساب زيادة مدة العملية.
// اضبط خاصية "MemoryOptimization" على "false" لحفظ المستند بتنسيق PDF بشكل طبيعي.
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

ينشئ كائن خيارات الحفظ لفئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | يحدد امتداد اسم هذا الملف فئة كائن خيارات الحفظ الذي سيتم إنشاؤه. |

### قيمة الإرجاع

كائن من فئة مشتق من[`SaveOptions`](../).

## أمثلة

يوضح كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.

```csharp
Document doc = new Document();

// تمكين تحديث النمط التلقائي، ولكن لا تقم بإرفاق مستند قالب.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// نظرًا لعدم وجود مستند قالب، لم يكن لدى المستند مكان لتتبع تغييرات الأسلوب.
// استخدم كائن SaveOptions لتعيين قالب تلقائيًا
// إذا كان المستند الذي نحفظه لا يحتوي على واحد.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
