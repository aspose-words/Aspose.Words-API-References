---
title: PdfSaveOptions.ExportDocumentStructure
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم تصدير بنية المستند أم لا.
type: docs
weight: 120
url: /ar/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

الحصول على أو تعيين قيمة تحدد ما إذا كان سيتم تصدير بنية المستند أم لا.

```csharp
public bool ExportDocumentStructure { get; set; }
```

### ملاحظات

يتم تجاهل هذه القيمة عند الحفظ في PDF / A-1a و PDF / A-2a و PDF / UA-1 لأن بنية المستند مطلوبة لهذا التوافق.

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة ، خاصة للمستندات الكبيرة.

### أمثلة

يوضح كيفية الحفاظ على عناصر بنية المستند ، والتي يمكن أن تساعد في تفسير وثيقتنا برمجيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "ExportDocumentStructure" على "true" لجعل بنية المستند ، مثل هذه العلامات ، متاحة عبر
// جزء التنقل "المحتوى" في Adobe Acrobat على حساب زيادة حجم الملف.
// اضبط خاصية "ExportDocumentStructure" على "false" لعدم تصدير بنية المستند.
options.ExportDocumentStructure = exportDocumentStructure;

// لنفترض أننا قمنا بتصدير بنية المستند أثناء حفظ هذا المستند. في هذه الحالة،
// يمكننا فتحه باستخدام Adobe Acrobat والعثور على علامات لعناصر مثل العنوان
// والفقرة التالية عبر "عرض" - >. "إظهار / إخفاء" - >. "أجزاء التنقل" - >. "العلامات".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


