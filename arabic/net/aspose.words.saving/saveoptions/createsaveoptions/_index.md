---
title: SaveOptions.CreateSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions طريقة. إنشاء كائن خيارات الحفظ لفئة مناسبة لتنسيق الحفظ المحدد.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

إنشاء كائن خيارات الحفظ لفئة مناسبة لتنسيق الحفظ المحدد.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | تنسيق الحفظ الذي يتم من أجله إنشاء كائن خيارات الحفظ. |

### قيمة الإرجاع

كائن من فئة مشتقة من[`SaveOptions`](../).

### أمثلة

يعرض خيارًا لتحسين استهلاك الذاكرة عند تقديم مستندات كبيرة إلى PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// اضبط خاصية "MemoryOptimization" على "true" لتقليل أثر الذاكرة لعمليات حفظ المستندات الكبيرة
// بتكلفة زيادة مدة العملية.
// قم بتعيين خاصية "MemoryOptimization" على "خطأ" لحفظ المستند بتنسيق PDF بشكل طبيعي.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

إنشاء كائن خيارات الحفظ لفئة مناسبة لامتداد الملف المحدد في اسم الملف المحدد.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | يحدد امتداد اسم الملف هذا فئة كائن خيارات الحفظ المراد إنشاؤه. |

### قيمة الإرجاع

كائن من فئة مشتقة من[`SaveOptions`](../).

### أمثلة

يوضح كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.

```csharp
Document doc = new Document();

// تمكين التحديث التلقائي للنمط ، لكن لا تقم بإرفاق مستند نموذج.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// نظرًا لعدم وجود مستند قالب ، لم يكن للمستند أي مكان لتعقب تغييرات النمط.
// استخدم كائن SaveOptions لتعيين قالب تلقائيًا
// إذا كان المستند الذي نحفظه لا يحتوي على واحد.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


